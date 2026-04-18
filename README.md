# Barzen Site Forms

Mobile-first HTML forms for site managers. Each form generates a branded PDF on-device and emails it to the builder with Cal on CC.

## Forms

| Form | File | Reference |
|---|---|---|
| Toolbox Talk Record | `Barzen_Toolbox_Talk_Mobile.html` | BP-WHS-F02 \| Rev 2 |
| Test & Tag Register | `Barzen_Test_and_Tag_Mobile.html` | BP-ELEC-F01 \| Rev 2 |

Landing page: `index.html` links both.

## Hosted URLs

Once GitHub Pages is enabled (Settings → Pages → source `main`, root), the forms are live at:

- Landing: `https://<org>.github.io/<repo>/`
- Toolbox Talk: `https://<org>.github.io/<repo>/Barzen_Toolbox_Talk_Mobile.html`
- Test & Tag: `https://<org>.github.io/<repo>/Barzen_Test_and_Tag_Mobile.html`

## How the forms work

1. Site manager opens the URL on their phone.
2. Picks the job → project, builder, site manager and builder email auto-fill from the embedded Job Matrix.
3. Fills in the remaining fields.
4. Taps **Generate PDF & Email**.
5. On mobile: the Web Share API attaches the PDF to the user's email app with recipients pre-filled. On desktop: the PDF downloads and the default email app opens for manual attach.

No data is stored or transmitted anywhere except the user's own email client. PDFs are generated entirely in-browser using jsPDF loaded from cdnjs.

## Updating the Job Matrix

Job, builder email, and site manager mappings are embedded as `var JOBS = [...]` and `var STAFF = [...]` inside each HTML file. Update both files when jobs or staff change, then commit.

## Form references

- `BP-WHS-F02` — WHS series, Form 02 (Toolbox Talk Record)
- `BP-ELEC-F01` — Electrical series, Form 01 (Test & Tag Register)
