### Master

* Adds the status indicator (spinner) to the statusbar which appears when flow is
  type checking, so that users can tell if everything type checked or if flow is
  just not finished yet. Indicator can be disabled by setting `flow.showStatus` to
  `false`. - [@gozala][] [#85](https://github.com/flowtype/flow-for-vscode/pull/85)
* Type checks code as you type. Only unsaved changes in an active document are
  considered (other unsaved documents are type checked by content on the disk).
  This feature can be disabled by setting `flow.runOnEdit` to `false` - [@gozala][]
  [#87](https://github.com/flowtype/flow-for-vscode/pull/87)
* Adds the [flowtype.org/try](http://flowtype.org/try/) like functionality to allow
  sketching, without setting up a project. Unsaved documents (ones created by
  `Files: New Untitled File` command) in `javascript` / `javascriptreact` mode and
  [`@flow` pragma](https://flowtype.org/docs/new-project.html#typechecking-your-files)
  will be typechecked as you type (assuming `flow.runOnEdit` is set to `true`). Please
  note that once file is saved, unless it's under project with `.flowconfig` it will
  no longer be type checked un further edits. - [@gozala]
  [#88](https://github.com/flowtype/flow-for-vscode/pull/88)

### 0.5.0

* Uses the absolute path to the `where` command provided by Windows - JPanneel #69
* Uses the new VS Code autocompletion API for functions - orta #51
* When you want to work on the flow-for-vscode project, pressing run will start the
  babel build watcher task - orta
* Adds support for *.js.flow files ( such as those generated by graphql-js ) which are 
  treated as common JavaScript files - orta
* Fixes "File not found" error with diagnostics when `flow status --json` provides
  non-absolute file paths - ryanashcraft #77

### 0.4.0

* Adds the ability to use flow from your project's node_modules folder. 
  This is a security risk ( see https://github.com/facebook/nuclide/issues/570) and so it
  is hidden behind a user setting of `useNPMPackagedFlow` which needs to be set to `true`
  for it to work. - orta #53
* Show flow errors that start at line 0 - orta #54 

[@gozala]:https://github.com/Gozala
