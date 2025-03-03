 
# Capybara - Storefront UI based theme for Vue Storefront

New default template theme for [Vue Storefront](https://github.com/DivanteLtd/vue-storefront), based on [Storefront UI](https://storefrontui.io/). 90% of the Capybara code is closed in the [Storefront UI library](https://github.com/DivanteLtd/storefront-ui). Thanks to it, Capybara can maintain its flexibility, but minimize the risk of errors.

 **🔨  Current status: Production Ready**

We have prepared [short introduction](https://github.com/DivanteLtd/vsf-capybara/blob/develop/CODING_STANDARDS.md) to our coding standards and conventions we are using in Capybara theme.
 
 
## 🔌  Installation
To be able to use new Capybara theme in your Vue Storefront installation, you need to:

1. Install `lerna` globally:

   ```
   npm install -g lerna
   ```

   or

   ```
   yarn global add lerna
   ```

1. Configure `vsf-capybara` repository as a git submodule in theme path of your Vue Storefront workspace, and then track `master` branch:

   ```
   git submodule add -b master https://github.com/DivanteLtd/vsf-capybara.git src/themes/capybara
   ```

1. Fetch all the data:

   ```
   git submodule update --init --remote
   ```
1. Generate `local.json` file from script `generate-local-config.js`:
   ```
   node src/themes/capybara/scripts/generate-local-config.js
   ```
1. Update Vue Storefront configuration by copying `local.json` file from `src/themes/capybara` to root `config` directory.
1. For Vue Storefront 1.12.3 and earlier include "children_data.*" as includeFields for category in default.json.
1. Update TypeScript compiler option in `tsconfig.json` in root directory: change value for `compilerOptions`**.**`paths`**.**`theme/*` from default theme `["src/themes/default/*"]` to brand new Capybara theme: `["src/themes/capybara/*"]`.
1. Download all dependencies and start development server:

   ```
   lerna bootstrap && yarn dev
   ```

1. That’s all! Now after opening your development server (http://localhost:3000 by default) you should see Vue Storefront with Capybara theme!  🎉

## Design customization

If you want to customize the Capybara designs you can start with [this amazing Figma file](https://www.figma.com/community/file/883240116671776403) by Aditya Patel from HotWax Commerce.
