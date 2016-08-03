# slate-edit-table

[![NPM version](https://badge.fury.io/js/slate-edit-table.svg)](http://badge.fury.io/js/slate-edit-table)

A Slate plugin to handle table edition.

### Install

```
npm install slate-edit-table
```

### Features

- Pressing <kbd>Up</kbd> and <kbd>Down</kbd>, move the cursor to next/previous row
- Pressing <kbd>Enter</kbd>, insert a new row
- Pressing <kbd>Tab</kbd>, move the select to next cell
- Pressing <kbd>Shift+Tab</kbd>, move the select to previous cell

### Simple Usage

```js
import EditTable from 'slate-edit-table'

const plugins = [
  EditTable()
]
```

#### Arguments

- ``[typeTable: String]`` — type for table
- ``[typeRow: String]`` — type for the rows.
- ``[typeCell: String]`` — type for the cells.

### Utilities and Transform

`slate-edit-table` exports utilities and transforms:

#### `utils.insertRow`

`plugin.utils.isSelectionInTable(state: State) => Boolean`

Return true if selection is inside a table.

#### `transforms.insertRow`

`plugin.transforms.insertRow(transform: Transform, at: Number?) => Transform`

Insert a new row after the current one or at the specific index (`at`).

#### `transforms.insertColumn`

`plugin.transforms.insertColumn(transform: Transform, at: Number?) => Transform`

Insert a new column after the current one or at the specific index (`at`).

#### `transforms.removeRow`

`plugin.transforms.insertRow(transform: Transform, at: Number?) => Transform`

Remove current row or the one at a specific index (`at`).

#### `transforms.removeColumn`

`plugin.transforms.insertColumn(transform: Transform, at: Number?) => Transform`

Remove current column or the one at a specific index (`at`).

#### `transforms.moveSelection`

`plugin.transforms.moveSelection(transform: Transform, column: Number, row: Number) => Transform`

Move the selection to a specific position in the table.
