# for-editor-saul

### props

| name        | type     | default                     | description                                                                                            |
| ----------- | -------- | --------------------------- | ------------------------------------------------------------------------------------------------------ |
| value       | String   | -                           | value                                                                                                  |
| language    | String / IWords  | en   | Default Language(zh-CN: Simplified Chinese, en: English, zh-TW: Traditional Chinese, jp: Japanese), support localization by following the `interface IWords`     |
| placeholder | String   | Begin editing...            | The default prompt text when the textarea is empty                                                     |
| lineNum     | Boolean  | true                        | Show lineNum                                                                                           |
| style       | Object   | -                           | editor styles                                                                                          |
| height      | String   | 600px                       | editor height                                                                                          |
| preview     | Boolean  | false                       | preview switch                                                                                         |
| expand      | Boolean  | false                       | fullscreen switch                                                                                      |
| subfield    | Boolean  | false                       | true: Double columns - Edit preview same screen(notice: preview: true), Single Columns - otherwise not |
| toolbar     | Object   | As in the following example | toolbars                                                                                               |
| outline     | Boolean  | true                        | Display outline list for markdown                                                                      |
| highlight   | Function | Hljs.highlightAuto          | Hljs (highlight.js)'s function --- highlightAuto                                                       |
| anchor | Boolean | true | Control if the anchor is displayed at the preview |

#### Localization

> IWords

```js
interface IWords {
  placeholder: string
  h1: string
  h2: string
  h3: string
  h4: string
  h5: string
  h6: string
  undo: string
  redo: string
  list: string
  orderlist: string
  disorderlist: string
  checklist: string
  para: string
  italic: string
  bold: string
  bolditalic: string
  delline: string
  underline: string
  keytext: string
  superscript: string
  subscript: string
  marktag: string
  quote: string
  table: string
  img: string
  link: string
  inlinecode: string
  code: string
  collapse: string
  katex: string
  save: string
  preview: string
  singleColumn: string
  doubleColumn: string
  fullscreenOn: string
  fullscreenOff: string
  addImgLink: string
  addImg: string
  toc: string
}
```

### events

| name     | params        | default | description                                 |
| -------- | ------------- | ------- | ------------------------------------------- |
| onChange | String: value | -       | Edit area change callback event             |
| onSave   | String: value | -       | Ctrl+s and click save button callback event |
| addImg   | File: file    | -       | upload image callback event                 |

### hot key

| name   | description |
| ------ | ----------- |
| tab    | two space   |
| ctrl+s | save        |
| ctrl+z | undo        |
| ctrl+y | redo        |
