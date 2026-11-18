# Canopy Studio Configurator

React + TypeScript MVP for the custom canopy tent technical test.

## Run

```bash
npm install
npm run dev
```

## Architecture

- `src/App.tsx` owns the structured configuration model and composes the workflow.
- React Three Fiber loads the provided GLB variants from `public/models`.
- The 2D editor uses the same configuration object as the 3D preview, so size, color, branding and placement stay synchronized.
- Pricing is represented by the `models` catalog and calculated customization fee; the Shopify action is an asynchronous mock integration that serializes the configuration as line-item properties.
- jsPDF creates a production summary with selections, price breakdown, branding placement, and a visual canopy preview.
- The layout is responsive and can be embedded in an iframe because it has no top-level navigation or origin-specific dependencies.

## Validation checklist

- [x] React + TypeScript
- [x] Fixed 10′ × 10′ product size with reference setup variants
- [x] Canopy + frame / canopy only / light-up frame
- [x] Side-wall and half-wall packages with single/double-sided options
- [x] Design notes and artwork upload
- [x] Color customization
- [x] Text and image-logo input
- [x] 2D branding placement
- [x] 3D preview with orbit and zoom
- [x] Shared structured configuration
- [x] Dynamic total pricing
- [x] Shopify-style cart payload
- [x] Production-summary PDF
- [x] Responsive layout
- [x] Production build passes

The pricing and Shopify integrations are intentionally mocked for the test and can be replaced with real endpoints without changing the configuration UI.
