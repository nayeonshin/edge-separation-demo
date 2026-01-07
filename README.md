# Pages vs Workers (Edge Separation Demo)

## Goal

Demonstrate why Cloudflare Pages and Workers are separate products even though both run at the edge:

- Pages = content delivery on page load
- Workers = request-level logic per HTTP request

## Live demo

- Pages: https://9976d00a.edge-separation-demo.pages.dev
- Worker: https://edge-separation-demo.nayeon.workers.dev/

## What to observe

1. Visiting the Pages URL loads static HTML (Pages trigger).
2. Clicking the button makes a cross-origin request to the Worker.
3. The Worker returns request/edge metadata (Workers trigger).

## Key takeaways

- Separation is about responsibility and trigger, not location.
- Pages serves frontend assets; Workers control request handling.
- Cross-origin integration requires CORS headers, which belong to request-level logic (Workers).
