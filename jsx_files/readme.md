# Interactive jsx documents

They are the basis for the HTML files in the root folder. You first generate interactive jsx visualization with Claude, then ask to convert into HTML for easier viewing.

Also comfortable is a dev server for generating HTML pages instantly for viewing.

## Steps:
* installation of vite (presenting layer)

    ```bash
    cd your-folder
    npm create vite@latest . -- --template react
    npm install
    npm install d3
    ```
* copy the fsx files into the src/ folder
  ```bash
    cp *.jsx src/
  ```
* evtl. edit src/App.css to show different jsx files
  ```bash
  -- add jsx files here and import them, then add them to the views object below

  import ValueChain from './cannabis_value_chain_DE'
  import WorldMap from './cannabis_world_map'

  const views = {
    WorldMap: <WorldMap />,
    ValueChain: <ValueChain />,
  }
  ```
* run the dev server and open localhost in browser
    ```bash
    npm run dev
    ```
