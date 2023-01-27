<div align="center">
    <h1>Svelte Iconoir</h1>
    <a href="https://github.com/indaco/svelte-iconoir/actions/workflows/release.yml" target="_blank">
        <img src="https://github.com/indaco/svelte-iconoir/actions/workflows/release.yml/badge.svg" alt="CI" />
    </a>
    &nbsp;
    <a href="https://www.npmjs.com/package/@indaco/svelte-iconoir" target="_blank"><img src="https://img.shields.io/npm/v/@indaco/svelte-iconoir.svg?style=flat" alt="NPM Package" /></a>
</div>

# Svelte Iconoir

> `svelte-iconoi@3.2.0` matches `iconoir@6.1`

## Description

This package provide the entire [iconoir](https://github.com/lucaburgio/iconoir) set (1000+ SVG icons) to be used with SvelteKit. It is based on the official [iconoir](https://github.com/lucaburgio/iconoir) project.

See all available icons on the **iconoir** [homepage](https://iconoir.com/)

## Install

```bash
# npm
npm install @indaco/svelte-iconoir

# pnpm
pnpm add @indaco/svelte-iconoir

# yarn
yarn add @indaco/svelte-iconoir
```

## Usage

Each icon is available to be used/imported following the **CamelCase** notation.

### 1. Direct

```html
<script>
 import { SunLightIcon } from '@indaco/svelte-iconoir';
 // to speed up dev server loading, use this
 import { ListIcon } from '@indaco/svelte-iconoir/icons/ListIcon';
</script>

<ListIcon />

<SunLightIcon class="roundedColor" />

<style>
 .roundedColor {
  padding: 4px;
  background-color: yellow;
  border-style: solid;
  border-color: #d1d5db;
 }
</style>
```

### 2. Inline styles

```html
<script>
 import { View360Icon } from '@indaco/svelte-iconoir/icons/View360Icon';
</script>

<View360Icon
 style="background-color: green; padding: 4px; border-radius: 9999px;"
 color="#ffffff" />
```

### 3. With Tailwind CSS

```html
<script>
 import { ActivityIcon } from '@indaco/svelte-iconoir/icons/ActivityIcon';
</script>

<ActivityIcon class="p-1 rounded-full border-2 bg-green-400" size="2.5em" />
```

## Properties

The `Iconoir` component has the following properties to allow you customing the rendered svg:

| Property | Type   | Required | Default           | Description                                 |
| :------- | :----- | :------: | :---------------- | :------------------------------------------ |
| alt      | String |    No    | same as icon name | Set the alt attribute on the rendered svg   |
| size     | String |    No    | `1.5em`           | Set the icon's size                         |
| color    | String |    No    | `currentColor`    | Set the icon's colour                       |
| style    | String |    No    |                   | Set the style attribute on the rendered svg |
| class    | String |    No    |                   | Set the class attribute on the rendered svg |

## Event Forwarding

You can also override the `click, dblclick` events on an element.

```html
<script>
 import { ActivityIcon } from '@indaco/svelte-iconoir/icons/ActivityIcon';
</script>

<ActivityIcon class="p-1 rounded-full border-6 bg-blue-300" on:click={() => alert("hi!")} size="2.5em" />
```

## Dev Flow

```bash
git clone https://github.com/indaco/svelte-iconoir.git

cd svelte-iconoir

# Install all dependencies
pnpm install # (or npm, yarn)

# Generate Svelte components for each icon
pnpm generate:icons

# Package
pnpm build
```

## License

Free and open-source software under the [MIT License](LICENSE)
