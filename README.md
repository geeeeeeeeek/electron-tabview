# [WIP] electron-tabview
Help you build a tab-based Electron app.

## Usage

```javascript
const TabView = require('electron-tabview');
```

## API

### TabView

```javascript
const tabView = new TabView();
```

#### Methods

##### `tabView.getTabGroup()`

Returns `TabGroup` - The handler of the tab group in the view.

##### `tabView.getActionGroup()`

Returns `ActionGroup` - The handler of the action group in the view.

### TabGroup

```javascript
const tabGroup = tabView.getTabGroup();
```

#### Methods

##### `tabGroup.addTab(options)`

- `options` Object
  - `title` *String* (optional, default is `null`) - The tab's title.
  - `icon` *String* (optional, default is empty) - The tab's icon url.
  - **`url`** *String* - The tab's content url. Provided for the webview.
  - `active` *Boolean* (optional, default is `false`). If set to true, the tab will be activated once mounted.
  - `closable` *Boolean* (optional, default is `false`) - Whether the tab is closable.
  - `onTabWillMount` *Function* (optional, default is `null`) - Executed before the tab will mount.
  - `onTabDidMount` *Function* (optional, default is `null`) - Executed after the tab mounted.
  - `onTabActivated` *Function* (optional, default is `null`) - Excuted when the tab is activated.

Returns `Tab` - The tab added to the group.