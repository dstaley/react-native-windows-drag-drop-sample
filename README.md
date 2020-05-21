# React Native for Windows Drag-and-drop Example

This project demonstrates how to add drag-and-drop support to a React Native for Windows project.

## DragDropModule.cs

The [main file](https://github.com/dstaley/react-native-windows-drag-drop-sample/blob/master/windows/DragAndDrop/DragDropModule.cs) in this project is the native module that registers the drag/drop event handlers on the native side.

### Init

The `init()` method is called from the React side, and sets up the entire window to accept drag/drop events. This method also registers the event handlers that dispatch the matching event.

### DragOverEvent

Called when a file is dragged over the window. Dispatches the `DragOverEvent` event in React.

### DragLeaveEvent

Called when a previously dragged file exits the window. Dispatches the `DragLeaveEvent` event in React.

### DropEvent

Called when dragged files are dropped onto the window. Dispatches the `DropEvent` event in React.

## App.js

[This file](https://github.com/dstaley/react-native-windows-drag-drop-sample/blob/master/App.js) demonstrates how to initialize the native module and subscribe to events.

## Thoughts

This is a super simple example, but it should provide enough of a base to customize for your specific usage. In particular, you'll probably want to convert the files to base64 encoded strings and pass them to React that way, especially if you're accepting binary files instead of pure-text files. You can read more about some of the customizations you can make to the native module in the [UWP Drag and Drop documentation](https://docs.microsoft.com/en-us/windows/uwp/design/input/drag-and-drop#customize-the-ui).
