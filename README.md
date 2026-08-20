# mdabashar.github.io

Academic homepage for Md Abul Bashar — <https://mdabashar.github.io/>

## Do not edit these files here

Everything in this repository is **deployed output**. The sources live in the
private `JobHunting` working folder, and the next deploy overwrites whatever is
here. Edits made directly in this repo will be silently lost.

| File | Where it comes from |
|---|---|
| `index.html` | hand-maintained in `JobHunting/site/` |
| `publications.html` | **generated** from `bashar_publications.bib` by `site/build_publications.py` |
| `style.css` | shared stylesheet, `JobHunting/site/` |
| `photo.jpg` | 600×600 crop of the source headshot |
| `robots.txt`, `sitemap.xml` | `JobHunting/site/` |

## Deploying

From the `JobHunting` folder:

```bash
bash site/deploy.sh
```

That rebuilds the publications page from the bibliography, runs `verify.py` to
check every factual claim against `master.yaml`, and refuses to publish if any
check fails — the live site is a public record, so a wrong citation count or a
superseded date should never reach it.

`master.yaml` is the single source of truth for facts that appear in more than
one document. Change it there first, then rebuild.
