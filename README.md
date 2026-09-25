# siralabs.org

Website of [Sira Labs](https://github.com/Sira-Labs): the organisation page and the product
pages (`/arqam/`). Plain HTML and one stylesheet, no build step; served by GitHub Pages from
`main` with the custom domain in `CNAME`. The repository is a project site
(`siralabs.github.io` under the `Sira-Labs` organisation), so it is only reachable at the
custom domain root; keep `CNAME` in place. DNS: four `A`/`AAAA` records for `@` to GitHub
Pages and `www` as a CNAME to `sira-labs.github.io`.

- `index.html` · Sira Labs (night theme)
- `arqam/index.html` · Arqam (sand theme)
- `assets/site.css` · shared styles; `assets/<brand>/` · marks, icons, screenshots and social
  previews, generated in `Sira-Labs/Arqam` by `docs/assets/genlogo.py`

The apps themselves are not served from this repository; the pages link to them on their
own subdomains:

- https://tabayyun.siralabs.org · Tabayyun (preview)
- https://suffa.siralabs.org · Suffa (preview)
- https://arqam-stg.siralabs.org · Arqam (preview)

All three are early previews for now (`.status.preview` chip on each card). When a project
leaves preview or moves, update its chip and links on the card in `index.html`, and the Arqam
page for Arqam.

Preview locally: `python3 -m http.server` in this folder, then open http://localhost:8000.
