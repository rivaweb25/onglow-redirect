# onglow.it → www.onglow.it

Questo repository serve solo a rimandare `onglow.it` (senza www) al sito vero,
`https://www.onglow.it`, mantenendo la pagina richiesta.

Perché esiste: il DNS di onglow.it resta su OVH (decisione del cliente) e il sito
sta su Cloudflare Pages con `www`. La radice di un dominio non accetta un CNAME,
e il redirect del pannello OVH non funziona in https. GitHub Pages accetta la
radice con quattro record A e gestisce il certificato da solo.

- Record su OVH: `onglow.it A` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
- Ogni pagina del sito ha qui una copia che rimanda alla stessa pagina su www
  (meta refresh + canonical); gli altri indirizzi passano da `404.html`.
- Codice del sito e storia della migrazione: repository OnGLOW, `migration/README.md`.
