# HeatShield

Heat checks for public streets. Add a photo of a road, bus shelter, roof or tree-lined street, and HeatShield shows where it soaks up the sun, who is most exposed, and which fixes would cool it down.

HeatShield is a student capstone project built on IEEE 7000-2021 and the ASCE Code of Ethics.

## What's in it

- **Analyze**: upload a photo (it stays on your device), see a sun absorption view, and get a worked example for that type of place: heat risks, before and after the fix, a weighted ethics score and the fixes to do first.
- **Photo check**: every upload is checked before analysis. The file type and size, that it opens, that no person fills the frame, and that it looks like an outdoor public space. Object detection runs in the browser with TensorFlow.js and COCO-SSD, so photos are never sent anywhere.
- **Audits**: example audit records for Los Angeles sites with search, filters and side-by-side comparison. Analyses you save are kept in your browser.
- **Examples, Fixes, Ethics**: worked examples, a library of cooling methods, and how the ethics score is calculated.

## Run it locally

It's a single static page with no build step.

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy

Import the repo into Vercel as a static site (no framework, no build command). `vercel.json` adds basic security headers.

## Limits

- It doesn't measure temperature. The sun absorption view and the rough surface estimate are based on photo brightness.
- The photo check can tell an outdoor place from a selfie or an indoor shot, but not a road from a roof. You pick the type.
- The sites and numbers are demonstration data. This is not a stamped engineering assessment.
