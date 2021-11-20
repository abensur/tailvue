<p align="center">
  <img src="https://raw.githubusercontent.com/fumeapp/tailvue/main/media/logo.png" width="300" alt="tailvue">
  <br />
  Vue components built for Vue3 powered by Windi CSS or tailwindcss
</p>

## 🚀 Features
- 🌔 All components and classes include dark-mode support
- 🔌 Programmatic toasts
<p align="center">
  <img src="https://raw.githubusercontent.com/fumeapp/tailvue/main/media/toast-demo.gif" alt="toasts">
</p>

```ts
$toast.show('this is a test');
```

<p align="center">
  <img src="https://raw.githubusercontent.com/fumeapp/tailvue/main/media/toast-singleaction.gif" alt="toasts-single-action">
</p>

```ts
$toast.show({
  type: 'danger',
  message: 'single action toast',
  timeout: 6,
  primary: {
    label: 'UNDO',
    action: () => $toast.show('you clicked UNDO')
  }
})
```

- 🔌 Programmatic modals
<p align="center">
  <img src="https://raw.githubusercontent.com/fumeapp/tailvue/main/media/modal-demo.gif" alt="modals">
</p>

```ts
$modal.show({
  type: 'danger',
  title: 'This is the title property',
  body: 'This is the body property.',
  primary: {
    label: 'Primary Action',
    theme: 'red',
    action: () => $toast.show('Primary Button clicked'),
  },
  secondary: {
    label: 'Secondary Action',
    theme: 'white',
    action: () => $toast.show('Clicked Secondary'),
  },
})
```

- 🎪 Interactive playground! - just run `yarn; yarn dev`
<p align="center">
  <img src="https://raw.githubusercontent.com/fumeapp/tailvue/main/media/playground.png" alt="playground">
</p>

- ✨ Tons of other components that will be documented shortly!


## Installation

### NuxtJS v3
```bash
yarn add --dev @tailvue/nuxt
```

* Add this to your `nuxt.config.ts`
```ts
buildModules: [
    '@tailvue/nuxt',
    ...,
],
```

### Vue3
```bash
yarn add tailvue
```

```ts
import { useToast, useModal } from 'tailvue'
const $toast = useToast()
const $modal = useModal()
```

### Icons
* All Icons supplied using the [Iconify Vue Component](https://docs.iconify.design/icon-components/vue/)
```bash
yarn add --dev @iconify/vue
```
