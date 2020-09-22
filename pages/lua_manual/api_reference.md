---
layout: page
title: Lua API Reference
status: improve
---

All instantiable classes define a `new()` function which returns an object of that particular class. 

With the exception of this `new()` function, all members listed will be member functions.

| Main |
| ---- |
| [Context](#Context) |
| [ContextDocumentsProxy](#ContextDocumentsProxy) |
| [DataFormatter](#DataFormatter) |
| [DataSource](#DataSource) |
| [Document](#Document) |
| [Element](#Element) |
| [ElementAttributesProxy](#ElementAttributesProxy) |
| [ElementChildNodesProxy](#ElementChildNodesProxy) |
| [ElementInstancer](#ElementInstancer) |
| [ElementPtr](#ElementPtr) |
| [ElementStyleProxy](#ElementStyleProxy) |
| [Event](#Event) |
| [EventParametersProxy](#EventParametersProxy) |
| [GlobalLuaFunctions](#GlobalLuaFunctions) |
| [Log](#Log) |
| [LuaDataSource](#LuaDataSource) |
| [rmlui](#rmlui) |
| [RmlUiContextsProxy](#RmlUiContextsProxy) |
| [SelectOptionsProxy](#SelectOptionsProxy) |

| Utility |
| ------- |
| [Colourb](#Colourb) |
| [Colourf](#Colourf) |
| [Vector2f](#Vector2f) |
| [Vector2i](#Vector2i) |

| Special Elements |
| ---------------- |
| [ElementDataGrid](#ElementDataGrid) |
| [ElementDataGridRow](#ElementDataGridRow) |
| [ElementForm](#ElementForm) |
| [ElementFormControl](#ElementFormControl) |
| [ElementFormControlDataSelect](#ElementFormControlDataSelect) |
| [ElementFormControlInput](#ElementFormControlInput) |
| [ElementFormControlSelect](#ElementFormControlSelect) |
| [ElementFormControlTextArea](#ElementFormControlTextArea) |
| [ElementTabSet](#ElementTabSet) |
| [ElementText](#ElementText) |

| Enumerations |
| ------------ |
| [DocumentFocus](#DocumentFocus) |
| [DocumentModal](#DocumentModal) |

---


## <a href='#Colourb' name='Colourb'>Colourb</a>

Inherits: `nil`{: .lua-type }

Constructs a colour with four channels, each from 0 to 255.

### Properties

| Name | Type |
| ------------ | ---- |
| [alpha](#Colourb-alpha){: .lua-function } | `integer`{: .lua-type } |
| [blue](#Colourb-blue){: .lua-function } | `integer`{: .lua-type } |
| [green](#Colourb-green){: .lua-function } | `integer`{: .lua-type } |
| [red](#Colourb-red){: .lua-function } | `integer`{: .lua-type } |
| [rgba](#Colourb-rgba){: .lua-function } | `integer, integer, integer, integer`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [new](#Colourb-new){: .lua-function }(`integer` red, `integer` green, `integer` blue, `integer` alpha) | `Colourb`{: .lua-type} |


### Metafunctions

| Metafunctions |
| ------------- |
| __add |
| __eq |
| __mul |


### Property Descriptions

####  `integer`{: .lua-type } <a href='#Colourb-alpha' name='Colourb-alpha'>alpha</a>{: .lua-function }

Alpha channel

####  `integer`{: .lua-type } <a href='#Colourb-blue' name='Colourb-blue'>blue</a>{: .lua-function }

Blue channel

####  `integer`{: .lua-type } <a href='#Colourb-green' name='Colourb-green'>green</a>{: .lua-function }

Green channel

####  `integer`{: .lua-type } <a href='#Colourb-red' name='Colourb-red'>red</a>{: .lua-function }

Red channel

####  `integer`{: .lua-type }, `integer`{: .lua-type }, `integer`{: .lua-type }, `integer`{: .lua-type } <a href='#Colourb-rgba' name='Colourb-rgba'>rgba</a>{: .lua-function }





### Function Descriptions

#### `Colourb`{: .lua-type} <a href='#Colourb-new' name='Colourb-new'>new</a>{: .lua-function }(`integer` red, `integer` green, `integer` blue, `integer` alpha)

Contruct a new `Colourb` object

---

## <a href='#Colourf' name='Colourf'>Colourf</a>

Inherits: `nil`{: .lua-type }

Constructs a colour with four floating point channels.

### Properties

| Name | Type |
| ------------ | ---- |
| [alpha](#Colourf-alpha){: .lua-function } | `number`{: .lua-type } |
| [blue](#Colourf-blue){: .lua-function } | `number`{: .lua-type } |
| [green](#Colourf-green){: .lua-function } | `number`{: .lua-type } |
| [red](#Colourf-red){: .lua-function } | `number`{: .lua-type } |
| [rgba](#Colourf-rgba){: .lua-function } | `number, number, number, number`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [new](#Colourf-new){: .lua-function }(`number` red, `number` green, `number` blue, `number` alpha) | `Colourf`{: .lua-type} |


### Metafunctions

| Metafunctions |
| ------------- |
| __eq |


### Property Descriptions

####  `number`{: .lua-type } <a href='#Colourf-alpha' name='Colourf-alpha'>alpha</a>{: .lua-function }

Alpha channel

####  `number`{: .lua-type } <a href='#Colourf-blue' name='Colourf-blue'>blue</a>{: .lua-function }

Blue channel

####  `number`{: .lua-type } <a href='#Colourf-green' name='Colourf-green'>green</a>{: .lua-function }

Green channel

####  `number`{: .lua-type } <a href='#Colourf-red' name='Colourf-red'>red</a>{: .lua-function }

Red channel

####  `number`{: .lua-type }, `number`{: .lua-type }, `number`{: .lua-type }, `number`{: .lua-type } <a href='#Colourf-rgba' name='Colourf-rgba'>rgba</a>{: .lua-function }





### Function Descriptions

#### `Colourf`{: .lua-type} <a href='#Colourf-new' name='Colourf-new'>new</a>{: .lua-function }(`number` red, `number` green, `number` blue, `number` alpha)

Construct a new `Colourf` object.

---

## <a href='#Context' name='Context'>Context</a>

Inherits: `nil`{: .lua-type }

The Context class has no constructor; it must be instantiated through the CreateContext() function. It has the following functions and properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [dimensions](#Context-dimensions){: .lua-function } | `Vector2i`{: .lua-type } |
| [documents](#Context-documents){: .lua-function } | `ContextDocumentsProxy`{: .lua-type } |
| [focus_element](#Context-focus_element){: .lua-function } | `Element`{: .lua-type } |
| [hover_element](#Context-hover_element){: .lua-function } | `Element`{: .lua-type } |
| [name](#Context-name){: .lua-function } | `string`{: .lua-type } |
| [root_element](#Context-root_element){: .lua-function } | `Element`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [AddEventListener](#Context-AddEventListener){: .lua-function }(`string`{: .lua-type } event, `function, string`{: .lua-type } script, `Element`{: .lua-type } element_context, `boolean`{: .lua-type } in_capture_phase) | `nil`{: .lua-type } |
| [CreateDocument](#Context-CreateDocument){: .lua-function }(`string`{: .lua-type } tag) | `Document`{: .lua-type }<br> |
| [LoadDocument](#Context-LoadDocument){: .lua-function }(`string`{: .lua-type } document_path) | `Document`{: .lua-type }<br> |
| [Render](#Context-Render){: .lua-function }() | `boolean`{: .lua-type }<br> |
| [UnloadAllDocuments](#Context-UnloadAllDocuments){: .lua-function }() | `nil`{: .lua-type } |
| [UnloadDocument](#Context-UnloadDocument){: .lua-function }(`Document`{: .lua-type } document) | `nil`{: .lua-type } |
| [Update](#Context-Update){: .lua-function }() | `boolean`{: .lua-type }<br> |


### Metafunctions




### Property Descriptions

####  `Vector2i`{: .lua-type } <a href='#Context-dimensions' name='Context-dimensions'>dimensions</a>{: .lua-function }

The dimensions of the context, as a Vector2i type.

####  `ContextDocumentsProxy`{: .lua-type } <a href='#Context-documents' name='Context-documents'>documents</a>{: .lua-function }

Returns an array of the documents within the context. This can be looked up as an array or a dictionary. Read-only.

####  `Element`{: .lua-type } <a href='#Context-focus_element' name='Context-focus_element'>focus_element</a>{: .lua-function }

Returns the leaf of the context's focus tree. Read-only.

####  `Element`{: .lua-type } <a href='#Context-hover_element' name='Context-hover_element'>hover_element</a>{: .lua-function }

Returns the element under the context's cursor. Read-only.

####  `string`{: .lua-type } <a href='#Context-name' name='Context-name'>name</a>{: .lua-function }

The name of the context, specified at construction. Read-only.

####  `Element`{: .lua-type } <a href='#Context-root_element' name='Context-root_element'>root_element</a>{: .lua-function }

Returns the context's root element. Read-only.



### Function Descriptions

#### `nil`{: .lua-type} <a href='#Context-AddEventListener' name='Context-AddEventListener'>AddEventListener</a>{: .lua-function }(`string`{: .lua-type } event, `function, string`{: .lua-type } script, `Element`{: .lua-type } element_context, `boolean`{: .lua-type } in_capture_phase)

Adds the inline Lua script or a Lua function, `script`, as an event listener to the context. `element_context` is an optional `Element`; if it is not `nil`, then the script will be executed as if it was bound to that element.

####  `Document`{: .lua-type } <a href='#Context-CreateDocument' name='Context-CreateDocument'>CreateDocument</a>{: .lua-function }(`string`{: .lua-type } tag)

Creates a new document with the tag name of `tag`.

####  `Document`{: .lua-type } <a href='#Context-LoadDocument' name='Context-LoadDocument'>LoadDocument</a>{: .lua-function }(`string`{: .lua-type } document_path)

Attempts to load a document from the RML file found at `document_path`. If successful, the document will be returned with a reference count of one.

####  `boolean`{: .lua-type } <a href='#Context-Render' name='Context-Render'>Render</a>{: .lua-function }()

Renders the context.

#### `nil`{: .lua-type} <a href='#Context-UnloadAllDocuments' name='Context-UnloadAllDocuments'>UnloadAllDocuments</a>{: .lua-function }()

Closes all documents currently loaded with the context.

#### `nil`{: .lua-type} <a href='#Context-UnloadDocument' name='Context-UnloadDocument'>UnloadDocument</a>{: .lua-function }(`Document`{: .lua-type } document)

Unloads a specific document within the context.

####  `boolean`{: .lua-type } <a href='#Context-Update' name='Context-Update'>Update</a>{: .lua-function }()

Updates the context.



---

## <a href='#ContextDocumentsProxy' name='ContextDocumentsProxy'>ContextDocumentsProxy</a>

Inherits: `nil`{: .lua-type }

Table of documents with the ability to be iterated over or indexed by an integer or a string.

### Properties




### Functions




### Metafunctions

| Metafunctions |
| ------------- |
| __index |
| __ipairs |
| __pairs |


### Property Descriptions



### Function Descriptions



---

## <a href='#DataFormatter' name='DataFormatter'>DataFormatter</a>

Inherits: `nil`{: .lua-type }

Lua data formatting helper.

### Properties

| Name | Type |
| ------------ | ---- |
| [FormatData](#DataFormatter-FormatData){: .lua-function } | `function`{: .lua-type } |

### Functions

| Name | Return Type |
| ------------ | ---- |
| [new](#DataFormatter-new){: .lua-function }(`nil, function`{: .lua-type } format_data) | `DataFormatter`{: .lua-type} |

### Metafunctions




### Property Descriptions

####  `function`{: .lua-type } <a href='#DataFormatter-FormatData' name='DataFormatter-FormatData'>FormatData</a>{: .lua-type }

Formatting function which returns a `string`

### Function Descriptions

#### `DataFormatter`{: .lua-type} <a href='#DataFormatter-new' name='DataFormatter-new'>new</a>{: .lua-function }(`nil, function`{: .lua-type } format_data)

Construct a new `DataFormatter` object. Optional `format_data` argument which is a function which returns a `string`.

---

## <a href='#DataSource' name='DataSource'>DataSource</a>

Inherits: `nil`{: .lua-type }

Abstract DataSource Interface.

### Properties




### Functions

| Name | Return Type |
| ------------ | ---- |
| [new](#DataSource-new){: .lua-function }(`string`{: .lua-type } name) | `DataSource`{: .lua-type }<br> |
| [GetNumRows](#DataSource-GetNumRows){: .lua-function }(`DataSource`{: .lua-type } table_name) | `integer`{: .lua-type }<br> |
| [GetRow](#DataSource-GetRow){: .lua-function }(`DataSource`{: .lua-type } table_name, `lua_type`{: .lua-type } index) | `string`{: .lua-type }<br> |
| [NotifyRowAdd](#DataSource-NotifyRowAdd){: .lua-function }(`string`{: .lua-type } table_name, `integer`{: .lua-type } first_row_added, `integer`{: .lua-type } num_rows_added) | `nil`{: .lua-type } |
| [NotifyRowChange](#DataSource-NotifyRowChange){: .lua-function }(`string`{: .lua-type } table_name, `nil, integer`{: .lua-type } first_row_changed, `nil, integer`{: .lua-type } num_rows_changed) | `nil`{: .lua-type } |
| [NotifyRowRemove](#DataSource-NotifyRowRemove){: .lua-function }(`string`{: .lua-type } table_name, `integer`{: .lua-type } first_row_removed, `integer`{: .lua-type } num_rows_removed) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions



### Function Descriptions

####  `DataSource`{: .lua-type } <a href='#DataSource-new' name='DataSource-new'>new</a>{: .lua-function }(`string`{: .lua-type } name)

Construct a new `DataSource` object.

####  `integer`{: .lua-type } <a href='#DataSource-GetNumRows' name='DataSource-GetNumRows'>GetNumRows</a>{: .lua-function }(`DataSource`{: .lua-type } table_name)

Return the number of rows in the given table

####  `string`{: .lua-type } <a href='#DataSource-GetRow' name='DataSource-GetRow'>GetRow</a>{: .lua-function }(`DataSource`{: .lua-type } table_name, `lua_type`{: .lua-type } index)

Return a list of the column values in string form

#### `nil`{: .lua-type} <a href='#DataSource-NotifyRowAdd' name='DataSource-NotifyRowAdd'>NotifyRowAdd</a>{: .lua-function }(`string`{: .lua-type } table_name, `integer`{: .lua-type } first_row_added, `integer`{: .lua-type } num_rows_added)

Notify listeners that rows have been added to the data source.

#### `nil`{: .lua-type} <a href='#DataSource-NotifyRowChange' name='DataSource-NotifyRowChange'>NotifyRowChange</a>{: .lua-function }(`string`{: .lua-type } table_name, `nil, integer`{: .lua-type } first_row_changed, `nil, integer`{: .lua-type } num_rows_changed)

Notify listeners that all rows on the data source have changed. Optional arguments `first_row_changed` for specifying the first row number which changed and `num_rows_changed` for specifying how many rows changed after the first row.

#### `nil`{: .lua-type} <a href='#DataSource-NotifyRowRemove' name='DataSource-NotifyRowRemove'>NotifyRowRemove</a>{: .lua-function }(`string`{: .lua-type } table_name, `integer`{: .lua-type } first_row_removed, `integer`{: .lua-type } num_rows_removed)

Notify listeners that rows have been removed from the data source.

---

## <a href='#DocumentFocus' name='DocumentFocus'>DocumentFocus</a>

Inherits: `nil`{: .lua-type }

Enum type used as an argument to various functions requiring focus options.

### Properties

| Name | Type |
| ------------ | ---- |
| [None](#DocumentFocus-None){: .lua-function } | `integer`{: .lua-type } |
| [Document](#DocumentFocus-Document){: .lua-function } | `integer`{: .lua-type } |
| [Keep](#DocumentFocus-Keep){: .lua-function } | `integer`{: .lua-type } |
| [Auto](#DocumentFocus-Auto){: .lua-function } | `integer`{: .lua-type } |

### Property Descriptions

####  `integer`{: .lua-type } <a href='#DocumentFocus-None' name='DocumentFocus-None'>None</a>{: .lua-function }

No focus.

####  `integer`{: .lua-type } <a href='#DocumentFocus-Document' name='DocumentFocus-Document'>Document</a>{: .lua-function }

Document focus.

####  `integer`{: .lua-type } <a href='#DocumentFocus-Keep' name='DocumentFocus-Keep'>Keep</a>{: .lua-function }

Keep focus.

####  `integer`{: .lua-type } <a href='#DocumentFocus-Auto' name='DocumentFocus-Auto'>Auto</a>{: .lua-function }

Auto focus.

---

## <a href='#DocumentModal' name='DocumentModal'>DocumentModal</a>

Inherits: `nil`{: .lua-type }

Enum type used as an argument to various functions requiring modal options.

### Properties

| Name | Type |
| ------------ | ---- |
| [None](#DocumentModal-None){: .lua-function } | `integer`{: .lua-type } |
| [Modal](#DocumentModal-Modal){: .lua-function } | `integer`{: .lua-type } |
| [Keep](#DocumentModal-Keep){: .lua-function } | `integer`{: .lua-type } |

### Property Descriptions

####  `integer`{: .lua-type } <a href='#DocumentModal-None' name='DocumentModal-None'>None</a>{: .lua-function }

No modal.

####  `integer`{: .lua-type } <a href='#DocumentModal-Modal' name='DocumentModal-Modal'>Modal</a>{: .lua-function }

Modal.

####  `integer`{: .lua-type } <a href='#DocumentModal-Keep' name='DocumentModal-Keep'>Keep</a>{: .lua-function }

Keep modal.

---

## <a href='#Document' name='Document'>Document</a>

Inherits: `Element`{: .lua-type }

Document derives from Element. Document has no constructor; it must be instantiated through a Context object instead, either by loading an external RML file or creating an empty document. It has the following functions and properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [context](#Document-context){: .lua-function } | `Context`{: .lua-type } |
| [title](#Document-title){: .lua-function } | `string`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [Close](#Document-Close){: .lua-function }() | `nil`{: .lua-type } |
| [CreateElement](#Document-CreateElement){: .lua-function }(`string`{: .lua-type } tag_name) | `ElementPtr`{: .lua-type }<br> |
| [CreateTextNode](#Document-CreateTextNode){: .lua-function }(`string`{: .lua-type } text) | `ElementPtr`{: .lua-type }<br> |
| [Hide](#Document-Hide){: .lua-function }() | `nil`{: .lua-type } |
| [PullToFront](#Document-PullToFront){: .lua-function }() | `nil`{: .lua-type } |
| [PushToBack](#Document-PushToBack){: .lua-function }() | `nil`{: .lua-type } |
| [Show](#Document-Show){: .lua-function }(`nil, DocumentModal`{: .lua-type } modal, `nil, DocumentFocus`{: .lua-type } focus) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

####  `Context`{: .lua-type } <a href='#Document-context' name='Document-context'>context</a>{: .lua-function }

The context the document belongs to. Read-only.

####  `string`{: .lua-type } <a href='#Document-title' name='Document-title'>title</a>{: .lua-function }

The title of the document, as initially set by the \<title\> tag in the document's header.



### Function Descriptions

#### `nil`{: .lua-type} <a href='#Document-Close' name='Document-Close'>Close</a>{: .lua-function }()

Hides and closes the document, destroying its contents.

####  `ElementPtr`{: .lua-type } <a href='#Document-CreateElement' name='Document-CreateElement'>CreateElement</a>{: .lua-function }(`string`{: .lua-type } tag_name)

Instances an element with a tag of tag_name.

####  `ElementPtr`{: .lua-type } <a href='#Document-CreateTextNode' name='Document-CreateTextNode'>CreateTextNode</a>{: .lua-function }(`string`{: .lua-type } text)

Instances a text element containing the string text.

#### `nil`{: .lua-type} <a href='#Document-Hide' name='Document-Hide'>Hide</a>{: .lua-function }()

Hides the document.

#### `nil`{: .lua-type} <a href='#Document-PullToFront' name='Document-PullToFront'>PullToFront</a>{: .lua-function }()

Pulls the document in front of other documents within its context with a similar z-index.

#### `nil`{: .lua-type} <a href='#Document-PushToBack' name='Document-PushToBack'>PushToBack</a>{: .lua-function }()

Pushes the document behind other documents within its context with a similar z-index.

#### `nil`{: .lua-type} <a href='#Document-Show' name='Document-Show'>Show</a>{: .lua-function }(`nil, DocumentModal`{: .lua-type } modal, `nil, DocumentFocus`{: .lua-type } focus)

Shows the document. Optional enum arguments to specify modal and focus mode. Defaults to `DocumentModal.None` and `DocumentFocus.Auto`.



---

## <a href='#Element' name='Element'>Element</a>

Inherits: `nil`{: .lua-type }

The Element class has no constructor; it must be instantiated through a [Document](#document) object instead. It has the following functions and properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [attributes](#Element-attributes){: .lua-function } | `ElementAttributesProxy`{: .lua-type } |
| [child_nodes](#Element-child_nodes){: .lua-function } | `ElementChildNodesProxy`{: .lua-type } |
| [class_name](#Element-class_name){: .lua-function } | `string`{: .lua-type } |
| [client_height](#Element-client_height){: .lua-function } | `number`{: .lua-type } |
| [client_left](#Element-client_left){: .lua-function } | `number`{: .lua-type } |
| [client_top](#Element-client_top){: .lua-function } | `number`{: .lua-type } |
| [client_width](#Element-client_width){: .lua-function } | `number`{: .lua-type } |
| [first_child](#Element-first_child){: .lua-function } | `nil, Element`{: .lua-type } |
| [id](#Element-id){: .lua-function } | `string`{: .lua-type } |
| [inner_rml](#Element-inner_rml){: .lua-function } | `string`{: .lua-type } |
| [last_child](#Element-last_child){: .lua-function } | `nil, Element`{: .lua-type } |
| [next_sibling](#Element-next_sibling){: .lua-function } | `nil, Element`{: .lua-type } |
| [offset_height](#Element-offset_height){: .lua-function } | `number`{: .lua-type } |
| [offset_left](#Element-offset_left){: .lua-function } | `number`{: .lua-type } |
| [offset_parent](#Element-offset_parent){: .lua-function } | `Element`{: .lua-type } |
| [offset_top](#Element-offset_top){: .lua-function } | `number`{: .lua-type } |
| [offset_width](#Element-offset_width){: .lua-function } | `number`{: .lua-type } |
| [owner_document](#Element-owner_document){: .lua-function } | `Document`{: .lua-type } |
| [parent_node](#Element-parent_node){: .lua-function } | `nil, Element`{: .lua-type } |
| [previous_sibling](#Element-previous_sibling){: .lua-function } | `nil, Element`{: .lua-type } |
| [scroll_height](#Element-scroll_height){: .lua-function } | `number`{: .lua-type } |
| [scroll_left](#Element-scroll_left){: .lua-function } | `number`{: .lua-type } |
| [scroll_top](#Element-scroll_top){: .lua-function } | `number`{: .lua-type } |
| [scroll_width](#Element-scroll_width){: .lua-function } | `number`{: .lua-type } |
| [style](#Element-style){: .lua-function } | `ElementStyleProxy`{: .lua-type } |
| [tag_name](#Element-tag_name){: .lua-function } | `string`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [AddEventListener](#Element-AddEventListener){: .lua-function }(`string`{: .lua-type } event, `function, string`{: .lua-type } listener, `boolean`{: .lua-type } in_capture_phase) | `nil`{: .lua-type } |
| [AppendChild](#Element-AppendChild){: .lua-function }(`ElementPtr`{: .lua-type } element) | `nil`{: .lua-type } |
| [Blur](#Element-Blur){: .lua-function }() | `nil`{: .lua-type } |
| [Click](#Element-Click){: .lua-function }() | `nil`{: .lua-type } |
| [DispatchEvent](#Element-DispatchEvent){: .lua-function }(`string`{: .lua-type } event, `table`{: .lua-type } parameters, `string`{: .lua-type } interruptible) | `nil`{: .lua-type }<br> |
| [new](#Element-new){: .lua-function }(`string`{: .lua-type } tag) | `Element`{: .lua-type} |
| [Focus](#Element-Focus){: .lua-function }() | `nil`{: .lua-type } |
| [GetAttribute](#Element-GetAttribute){: .lua-function }(`string`{: .lua-type } name) | `Variant`{: .lua-type }<br> |
| [GetElementById](#Element-GetElementById){: .lua-function }(`string`{: .lua-type } id) | `Element`{: .lua-type }<br> |
| [GetElementsByTagName](#Element-GetElementsByTagName){: .lua-function }(`string`{: .lua-type } tag_name) | `table`{: .lua-type }<br> |
| [HasAttribute](#Element-HasAttribute){: .lua-function }(`string`{: .lua-type } name) | `boolean`{: .lua-type }<br> |
| [HasChildNodes](#Element-HasChildNodes){: .lua-function }() | `boolean`{: .lua-type }<br> |
| [InsertBefore](#Element-InsertBefore){: .lua-function }(`ElementPtr`{: .lua-type } element, `Element`{: .lua-type } adjacent_element) | `nil`{: .lua-type } |
| [IsClassSet](#Element-IsClassSet){: .lua-function }(`string`{: .lua-type } name) | `boolean`{: .lua-type }<br> |
| [RemoveAttribute](#Element-RemoveAttribute){: .lua-function }(`string`{: .lua-type } name) | `nil`{: .lua-type } |
| [RemoveChild](#Element-RemoveChild){: .lua-function }(`Element`{: .lua-type } element) | `boolean`{: .lua-type }<br> |
| [ReplaceChild](#Element-ReplaceChild){: .lua-function }(`ElementPtr`{: .lua-type } inserted_element, `Element`{: .lua-type } replaced_element) | `boolean`{: .lua-type }<br> |
| [ScrollIntoView](#Element-ScrollIntoView){: .lua-function }(`boolean`{: .lua-type } align_with_top) | `nil`{: .lua-type } |
| [SetAttribute](#Element-SetAttribute){: .lua-function }(`string`{: .lua-type } name, `string`{: .lua-type } value) | `nil`{: .lua-type } |
| [SetClass](#Element-SetClass){: .lua-function }(`string`{: .lua-type } name, `boolean`{: .lua-type } value) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

####  `ElementAttributesProxy`{: .lua-type } <a href='#Element-attributes' name='Element-attributes'>attributes</a>{: .lua-function }

The array of attributes on the element. Each element has the read-only properties name and value. Read-only.

####  `ElementChildNodesProxy`{: .lua-type } <a href='#Element-child_nodes' name='Element-child_nodes'>child_nodes</a>{: .lua-function }

The array of child nodes on the element. Read-only.

####  `string`{: .lua-type } <a href='#Element-class_name' name='Element-class_name'>class_name</a>{: .lua-function }

The space-separated list of classes on the element.

####  `number`{: .lua-type } <a href='#Element-client_height' name='Element-client_height'>client_height</a>{: .lua-function }

The height of the element's client area. Read-only.

####  `number`{: .lua-type } <a href='#Element-client_left' name='Element-client_left'>client_left</a>{: .lua-function }

The distance between the left border edge and the left client edge of the element. Read-only.

####  `number`{: .lua-type } <a href='#Element-client_top' name='Element-client_top'>client_top</a>{: .lua-function }

The distance between the top border edge and the top client edge of the element. Read-only.

####  `number`{: .lua-type } <a href='#Element-client_width' name='Element-client_width'>client_width</a>{: .lua-function }

The width of the element's client area. Read-only.

####  `nil`{: .lua-type }, `Element`{: .lua-type } <a href='#Element-first_child' name='Element-first_child'>first_child</a>{: .lua-function }

The first child of the element, or `nil` if the client has no children. Read-only.

####  `string`{: .lua-type } <a href='#Element-id' name='Element-id'>id</a>{: .lua-function }

The ID of the element, or the empty string if the element has no ID.

####  `string`{: .lua-type } <a href='#Element-inner_rml' name='Element-inner_rml'>inner_rml</a>{: .lua-function }

The element's RML content.

####  `nil`{: .lua-type }, `Element`{: .lua-type } <a href='#Element-last_child' name='Element-last_child'>last_child</a>{: .lua-function }

The last child of the element, or `nil` if the client has no children. Read-only.

####  `nil`{: .lua-type }, `Element`{: .lua-type } <a href='#Element-next_sibling' name='Element-next_sibling'>next_sibling</a>{: .lua-function }

The element's next sibling, or `nil` if it is the last sibling. Read-only.

####  `number`{: .lua-type } <a href='#Element-offset_height' name='Element-offset_height'>offset_height</a>{: .lua-function }

The height of the element, excluding margins. Read-only.

####  `number`{: .lua-type } <a href='#Element-offset_left' name='Element-offset_left'>offset_left</a>{: .lua-function }

The distance between the element's offset parent's left border edge and this element's left border edge. Read-only.

####  `Element`{: .lua-type } <a href='#Element-offset_parent' name='Element-offset_parent'>offset_parent</a>{: .lua-function }

The element's offset parent. Read only.

####  `number`{: .lua-type } <a href='#Element-offset_top' name='Element-offset_top'>offset_top</a>{: .lua-function }

The distance between the element's offset parent's top border edge and this element's top border edge. Read-only.

####  `number`{: .lua-type } <a href='#Element-offset_width' name='Element-offset_width'>offset_width</a>{: .lua-function }

The width of the element, excluding margins. Read-only.

####  `Document`{: .lua-type } <a href='#Element-owner_document' name='Element-owner_document'>owner_document</a>{: .lua-function }

The document this element is part of. Read-only.

####  `nil`{: .lua-type }, `Element`{: .lua-type } <a href='#Element-parent_node' name='Element-parent_node'>parent_node</a>{: .lua-function }

The element this element is directly parented to. Read-only.

####  `nil`{: .lua-type }, `Element`{: .lua-type } <a href='#Element-previous_sibling' name='Element-previous_sibling'>previous_sibling</a>{: .lua-function }

The element's previous sibling, or None if it is the first sibling. Read-only.

####  `number`{: .lua-type } <a href='#Element-scroll_height' name='Element-scroll_height'>scroll_height</a>{: .lua-function }

The height of this element's content. This will be at least as high as the client height. Read-only.

####  `number`{: .lua-type } <a href='#Element-scroll_left' name='Element-scroll_left'>scroll_left</a>{: .lua-function }

The offset between the left edge of this element's client area and the left edge of the content area.

####  `number`{: .lua-type } <a href='#Element-scroll_top' name='Element-scroll_top'>scroll_top</a>{: .lua-function }

The offset between the top edge of this element's client area and the top edge of the content area.

####  `number`{: .lua-type } <a href='#Element-scroll_width' name='Element-scroll_width'>scroll_width</a>{: .lua-function }

The width of this element's content. This will be at least as wide as the client width. Read-only.

####  `ElementStyleProxy`{: .lua-type } <a href='#Element-style' name='Element-style'>style</a>{: .lua-function }

An object used to access this element's style information. Individual RCSS properties can be accessed by using the name of the property as a Lua property on the object itself (ie, element.style.width = "40px").

####  `string`{: .lua-type } <a href='#Element-tag_name' name='Element-tag_name'>tag_name</a>{: .lua-function }

The tag name used to instance this element. Read-only.



### Function Descriptions

#### `nil`{: .lua-type} <a href='#Element-AddEventListener' name='Element-AddEventListener'>AddEventListener</a>{: .lua-function }(`string`{: .lua-type } event, `function, string`{: .lua-type } listener, `boolean`{: .lua-type } in_capture_phase)

NOTE: Events added from Lua cannot be removed.

#### `nil`{: .lua-type} <a href='#Element-AppendChild' name='Element-AppendChild'>AppendChild</a>{: .lua-function }(`ElementPtr`{: .lua-type } element)

Appends element as a child to this element.

#### `nil`{: .lua-type} <a href='#Element-Blur' name='Element-Blur'>Blur</a>{: .lua-function }()

Removes input focus from this element.

#### `nil`{: .lua-type} <a href='#Element-Click' name='Element-Click'>Click</a>{: .lua-function }()

Fakes a click on this element.

####  `nil`{: .lua-type } <a href='#Element-DispatchEvent' name='Element-DispatchEvent'>DispatchEvent</a>{: .lua-function }(`string`{: .lua-type } event, `table`{: .lua-type } parameters, `string`{: .lua-type } interruptible)

Dispatches an event to this element. The event is of type event. Parameters to the event are given in the dictionary parameters; the dictionary must only contain string keys and floating-point, integer or string values. interruptible determines if the event can be forced to stop propagation early.

#### `Element`{: .lua-type} <a href='#Element-new' name='Element-new'>new</a>{: .lua-function }(`string`{: .lua-type } tag)

Construct new `Element` object.

#### `nil`{: .lua-type} <a href='#Element-Focus' name='Element-Focus'>Focus</a>{: .lua-function }()

Gives input focus to this element.

####  `Variant`{: .lua-type } <a href='#Element-GetAttribute' name='Element-GetAttribute'>GetAttribute</a>{: .lua-function }(`string`{: .lua-type } name)

Returns the value of the attribute named name. If no such attribute exists, the empty string will be returned.

####  `Element`{: .lua-type } <a href='#Element-GetById' name='Element-GetById'>GetById</a>{: .lua-function }(`string`{: .lua-type } id)

Returns the descendant element with an id of id.

####  `table`{: .lua-type } <a href='#Element-GetsByTagName' name='Element-GetsByTagName'>GetsByTagName</a>{: .lua-function }(`string`{: .lua-type } tag_name)

Returns a list of all descendant elements with the tag of `tag_name`. Returned table is indexable with integers.

####  `boolean`{: .lua-type } <a href='#Element-HasAttribute' name='Element-HasAttribute'>HasAttribute</a>{: .lua-function }(`string`{: .lua-type } name)

Returns true if the element has a value for the attribute named name, false if not.

####  `boolean`{: .lua-type } <a href='#Element-HasChildNodes' name='Element-HasChildNodes'>HasChildNodes</a>{: .lua-function }()

Returns true if the element has at least one child node, false if not.

#### `nil`{: .lua-type} <a href='#Element-InsertBefore' name='Element-InsertBefore'>InsertBefore</a>{: .lua-function }(`ElementPtr`{: .lua-type } element, `Element`{: .lua-type } adjacent_element)

Inserts the element element as a child of this element, directly before adjacent_element in the list of children.

####  `boolean`{: .lua-type } <a href='#Element-IsClassSet' name='Element-IsClassSet'>IsClassSet</a>{: .lua-function }(`string`{: .lua-type } name)

Returns true if the class name is set on the element, false if not.

#### `nil`{: .lua-type} <a href='#Element-RemoveAttribute' name='Element-RemoveAttribute'>RemoveAttribute</a>{: .lua-function }(`string`{: .lua-type } name)

Removes the attribute named name from the element.

####  `boolean`{: .lua-type } <a href='#Element-RemoveChild' name='Element-RemoveChild'>RemoveChild</a>{: .lua-function }(`Element`{: .lua-type } element)

Removes the child element element from this element.

####  `boolean`{: .lua-type } <a href='#Element-ReplaceChild' name='Element-ReplaceChild'>ReplaceChild</a>{: .lua-function }(`ElementPtr`{: .lua-type } inserted_element, `Element`{: .lua-type } replaced_element)

Replaces the child element replaced_element with `inserted_element` in this element's list of children. If replaced_element is not a child of this element, `inserted_element` will be appended onto the list instead.

#### `nil`{: .lua-type} <a href='#Element-ScrollIntoView' name='Element-ScrollIntoView'>ScrollIntoView</a>{: .lua-function }(`boolean`{: .lua-type } align_with_top)

Scrolls this element into view if its ancestors have hidden overflow. If `align_with_top` is true, the element's top edge will be aligned with the top (or as close as possible to the top) of its ancestors' viewing windows. If false, its bottom edge will be aligned to the bottom.

#### `nil`{: .lua-type} <a href='#Element-SetAttribute' name='Element-SetAttribute'>SetAttribute</a>{: .lua-function }(`string`{: .lua-type } name, `string`{: .lua-type } value)

Sets the value of the attribute named name to value.

#### `nil`{: .lua-type} <a href='#Element-SetClass' name='Element-SetClass'>SetClass</a>{: .lua-function }(`string`{: .lua-type } name, `boolean`{: .lua-type } value)

Sets (if value is true) or clears (if value is false) the class name on the element.



---

## <a href='#ElementAttributesProxy' name='ElementAttributesProxy'>ElementAttributesProxy</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions




### Metafunctions

| Metafunctions |
| ------------- |
| __index |
| __ipairs |
| __pairs |


### Property Descriptions



### Function Descriptions



---

## <a href='#ElementChildNodesProxy' name='ElementChildNodesProxy'>ElementChildNodesProxy</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions




### Metafunctions

| Metafunctions |
| ------------- |
| __index |
| __ipairs |
| __pairs |


### Property Descriptions



### Function Descriptions



---

## <a href='#ElementDataGrid' name='ElementDataGrid'>ElementDataGrid</a>

Inherits: `Element`{: .lua-type }

ElementDataGrid derives from Element. The data grid has the following functions and properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [rows](#ElementDataGrid-rows){: .lua-function } | `table`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [AddColumn](#ElementDataGrid-AddColumn){: .lua-function }(`string`{: .lua-type } fields, `string`{: .lua-type } formatter, `number`{: .lua-type } initial_width, `string`{: .lua-type } header_rml) | `nil`{: .lua-type } |
| [SetDataSource](#ElementDataGrid-SetDataSource){: .lua-function }(`string`{: .lua-type } data_source_name) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

####  `table`{: .lua-type } <a href='#ElementDataGrid-rows' name='ElementDataGrid-rows'>rows</a>{: .lua-function }

Returns an array containing all the rows in the data grid.



### Function Descriptions

#### `nil`{: .lua-type} <a href='#ElementDataGrid-AddColumn' name='ElementDataGrid-AddColumn'>AddColumn</a>{: .lua-function }(`string`{: .lua-type } fields, `string`{: .lua-type } formatter, `number`{: .lua-type } initial_width, `string`{: .lua-type } header_rml)

Adds a new column to the data grid. The column will read the columns fields (in CSV format) from the grid's data source, processing it through the data formatter named formatter. `header_rml` specifies the RML content of the column's header.

#### `nil`{: .lua-type} <a href='#ElementDataGrid-SetDataSource' name='ElementDataGrid-SetDataSource'>SetDataSource</a>{: .lua-function }(`string`{: .lua-type } data_source_name)

Sets the name and table of the new data source to be used by the data grid.



---

## <a href='#ElementDataGridRow' name='ElementDataGridRow'>ElementDataGridRow</a>

Inherits: `Element`{: .lua-type }

ElementDataGridRow derives from Element. The data grid row has the following properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [parent_grid](#ElementDataGridRow-parent_grid){: .lua-function } | `ElementDataGrid`{: .lua-type } |
| [parent_relative_index](#ElementDataGridRow-parent_relative_index){: .lua-function } | `integer`{: .lua-type } |
| [parent_row](#ElementDataGridRow-parent_row){: .lua-function } | `ElementDataGridRow`{: .lua-type } |
| [row_expanded](#ElementDataGridRow-row_expanded){: .lua-function } | `boolean`{: .lua-type } |
| [table_relative_index](#ElementDataGridRow-table_relative_index){: .lua-function } | `integer`{: .lua-type } |


### Functions




### Metafunctions




### Property Descriptions

####  `ElementDataGrid`{: .lua-type } <a href='#ElementDataGridRow-parent_grid' name='ElementDataGridRow-parent_grid'>parent_grid</a>{: .lua-function }

The data grid that this row belongs to.

####  `integer`{: .lua-type } <a href='#ElementDataGridRow-parent_relative_index' name='ElementDataGridRow-parent_relative_index'>parent_relative_index</a>{: .lua-function }

The index of the row, relative to its parent row. So if you are the third row in your parent, then it will be 3.

####  `ElementDataGridRow`{: .lua-type } <a href='#ElementDataGridRow-parent_row' name='ElementDataGridRow-parent_row'>parent_row</a>{: .lua-function }

The parent row of this row. None if it at the top level.

####  `boolean`{: .lua-type } <a href='#ElementDataGridRow-row_expanded' name='ElementDataGridRow-row_expanded'>row_expanded</a>{: .lua-function }

The expanded state of the row, either true or false.

####  `integer`{: .lua-type } <a href='#ElementDataGridRow-table_relative_index' name='ElementDataGridRow-table_relative_index'>table_relative_index</a>{: .lua-function }

The index of the row, relative to the data grid it is in. This takes into account all previous rows and their children.



### Function Descriptions



---

## <a href='#ElementForm' name='ElementForm'>ElementForm</a>

Inherits: `Element`{: .lua-type }

ElementForm derives from Element. The form element has the following function:

### Properties




### Functions

| Name | Return Type |
| ------------ | ---- |
| [Submit](#ElementForm-Submit){: .lua-function }(`nil, string`{: .lua-type } name, `nil, string`{: .lua-type } submit_value) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions



### Function Descriptions

#### `nil`{: .lua-type} <a href='#ElementForm-Submit' name='ElementForm-Submit'>Submit</a>{: .lua-function }(`nil, string`{: .lua-type } name, `nil, string`{: .lua-type } submit_value)

Submits the form with name of `name` and a submit value of `submit_value`. `name` and `value` are optional and are empty by default.



---

## <a href='#ElementFormControl' name='ElementFormControl'>ElementFormControl</a>

Inherits: `Element`{: .lua-type }



### Properties

| Name | Type |
| ------------ | ---- |
| [disabled](#ElementFormControl-disabled){: .lua-function } | `boolean`{: .lua-type } |
| [name](#ElementFormControl-name){: .lua-function } | `string`{: .lua-type } |
| [value](#ElementFormControl-value){: .lua-function } | `string`{: .lua-type } |


### Functions




### Metafunctions




### Property Descriptions

####  `boolean`{: .lua-type } <a href='#ElementFormControl-disabled' name='ElementFormControl-disabled'>disabled</a>{: .lua-function }



####  `string`{: .lua-type } <a href='#ElementFormControl-name' name='ElementFormControl-name'>name</a>{: .lua-function }



####  `string`{: .lua-type } <a href='#ElementFormControl-value' name='ElementFormControl-value'>value</a>{: .lua-function }





### Function Descriptions



---

## <a href='#ElementFormControlDataSelect' name='ElementFormControlDataSelect'>ElementFormControlDataSelect</a>

Inherits: `ElementFormControlSelect`{: .lua-type }

ElementFormControlDataSelect derives from ElementFormControlSelect. It has the following additional function:

### Properties




### Functions

| Name | Return Type |
| ------------ | ---- |
| [SetDataSource](#ElementFormControlDataSelect-SetDataSource){: .lua-function }(`string`{: .lua-type } data_source_name) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions



### Function Descriptions

#### `nil`{: .lua-type} <a href='#ElementFormControlDataSelect-SetDataSource' name='ElementFormControlDataSelect-SetDataSource'>SetDataSource</a>{: .lua-function }(`string`{: .lua-type } data_source_name)

Sets the name and table of the new data source to be used by the select box.



---

## <a href='#ElementFormControlInput' name='ElementFormControlInput'>ElementFormControlInput</a>

Inherits: `ElementFormControl`{: .lua-type }

ElementFormControlInput derives from IElementFormControl. The control has the following properties, only appropriate on the relevant types:

### Properties

| Name | Type |
| ------------ | ---- |
| [checked](#ElementFormControlInput-checked){: .lua-function } | `boolean`{: .lua-type } |
| [max](#ElementFormControlInput-max){: .lua-function } | `integer`{: .lua-type } |
| [maxlength](#ElementFormControlInput-maxlength){: .lua-function } | `integer`{: .lua-type } |
| [min](#ElementFormControlInput-min){: .lua-function } | `integer`{: .lua-type } |
| [size](#ElementFormControlInput-size){: .lua-function } | `integer`{: .lua-type } |
| [step](#ElementFormControlInput-step){: .lua-function } | `integer`{: .lua-type } |


### Functions




### Metafunctions




### Property Descriptions

####  `boolean`{: .lua-type } <a href='#ElementFormControlInput-checked' name='ElementFormControlInput-checked'>checked</a>{: .lua-function }

Relevant for radio and checkbox types. The checked status of the input.

####  `integer`{: .lua-type } <a href='#ElementFormControlInput-max' name='ElementFormControlInput-max'>max</a>{: .lua-function }

Relevant for range types. The value of the control on the bottom / right of the slider.

####  `integer`{: .lua-type } <a href='#ElementFormControlInput-maxlength' name='ElementFormControlInput-maxlength'>maxlength</a>{: .lua-function }



####  `integer`{: .lua-type } <a href='#ElementFormControlInput-min' name='ElementFormControlInput-min'>min</a>{: .lua-function }

Relevant for range types. The value of the control on the top / left of the slider.

####  `integer`{: .lua-type } <a href='#ElementFormControlInput-size' name='ElementFormControlInput-size'>size</a>{: .lua-function }

Relevant for text types. The approximate number of characters the text field shows horizontally at once.

####  `integer`{: .lua-type } <a href='#ElementFormControlInput-step' name='ElementFormControlInput-step'>step</a>{: .lua-function }

Relevant for range types. The step the control's value changes in.



### Function Descriptions



---

## <a href='#ElementFormControlSelect' name='ElementFormControlSelect'>ElementFormControlSelect</a>

Inherits: `ElementFormControl`{: .lua-type }

ElementFormControlSelect derives from IElementFormControl. The control has the following functions and properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [options](#ElementFormControlSelect-options){: .lua-function } | `SelectOptionsProxy`{: .lua-type } |
| [selection](#ElementFormControlSelect-selection){: .lua-function } | `integer`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [Add](#ElementFormControlSelect-Add){: .lua-function }(`string`{: .lua-type } rml, `string`{: .lua-type } value, `nil, integer`{: .lua-type } before) | `integer`{: .lua-type }<br> |
| [Remove](#ElementFormControlSelect-Remove){: .lua-function }(`integer`{: .lua-type } index) | `nil`{: .lua-type } |
| [RemoveAll](#ElementFormControlSelect-RemoveAll){: .lua-function }() | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

####  `SelectOptionsProxy`{: .lua-type } <a href='#ElementFormControlSelect-options' name='ElementFormControlSelect-options'>options</a>{: .lua-function }

The array of options available in the select box. Each entry in the array has the property value, the string value of the option, and element, the root of the element hierarchy that represents the option in the list.

####  `integer`{: .lua-type } <a href='#ElementFormControlSelect-selection' name='ElementFormControlSelect-selection'>selection</a>{: .lua-function }

The index of the currently selected option.



### Function Descriptions

####  `integer`{: .lua-type } <a href='#ElementFormControlSelect-Add' name='ElementFormControlSelect-Add'>Add</a>{: .lua-function }(`string`{: .lua-type } rml, `string`{: .lua-type } value, `nil, integer`{: .lua-type } before)

Adds a new option to the select box. The new option has the string value of value and is represented by the elements created by the RML string rml. The new option will be inserted by the index specified by before; if this is out of bounds (the default), then the new option will be appended onto the list. The index of the new option will be returned.

#### `nil`{: .lua-type} <a href='#ElementFormControlSelect-Remove' name='ElementFormControlSelect-Remove'>Remove</a>{: .lua-function }(`integer`{: .lua-type } index)

Removes an existing option from the selection box.

#### `nil`{: .lua-type} <a href='#ElementFormControlSelect-RemoveAll' name='ElementFormControlSelect-RemoveAll'>RemoveAll</a>{: .lua-function }()





---

## <a href='#ElementFormControlTextArea' name='ElementFormControlTextArea'>ElementFormControlTextArea</a>

Inherits: `ElementFormControl`{: .lua-type }

ElementFormControlTextArea derives from IElementFormControl. The control has the following properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [cols](#ElementFormControlTextArea-cols){: .lua-function } | `integer`{: .lua-type } |
| [maxlength](#ElementFormControlTextArea-maxlength){: .lua-function } | `integer`{: .lua-type } |
| [rows](#ElementFormControlTextArea-rows){: .lua-function } | `integer`{: .lua-type } |
| [wordwrap](#ElementFormControlTextArea-wordwrap){: .lua-function } | `boolean`{: .lua-type } |


### Functions




### Metafunctions




### Property Descriptions

####  `integer`{: .lua-type } <a href='#ElementFormControlTextArea-cols' name='ElementFormControlTextArea-cols'>cols</a>{: .lua-function }

The approximate number of characters the text area shows horizontally at once.

####  `integer`{: .lua-type } <a href='#ElementFormControlTextArea-maxlength' name='ElementFormControlTextArea-maxlength'>maxlength</a>{: .lua-function }



####  `integer`{: .lua-type } <a href='#ElementFormControlTextArea-rows' name='ElementFormControlTextArea-rows'>rows</a>{: .lua-function }

The number of lines the text area shows at once.

####  `boolean`{: .lua-type } <a href='#ElementFormControlTextArea-wordwrap' name='ElementFormControlTextArea-wordwrap'>wordwrap</a>{: .lua-function }





### Function Descriptions



---

## <a href='#ElementInstancer' name='ElementInstancer'>ElementInstancer</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions

| Name | Return Type |
| ------------ | ---- |
| [new](#ElementInstancer-new){: .lua-function }() | `ElementInstancer`{: .lua-type} |
| [InstanceElement](#ElementInstancer-InstanceElement){: .lua-function }(`ElementInstancer`{: .lua-type } ) | `value`{: .lua-type }<br> |


### Metafunctions




### Property Descriptions



### Function Descriptions

#### `ElementInstancer`{: .lua-type} <a href='#ElementInstancer-new' name='ElementInstancer-new'>new</a>{: .lua-function }()



####  `value`{: .lua-type } <a href='#ElementInstancer-InstanceElement' name='ElementInstancer-InstanceElement'>InstanceElement</a>{: .lua-function }(`ElementInstancer`{: .lua-type } )





---

## <a href='#ElementPtr' name='ElementPtr'>ElementPtr</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions




### Metafunctions




### Property Descriptions



### Function Descriptions



---

## <a href='#ElementStyleProxy' name='ElementStyleProxy'>ElementStyleProxy</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions




### Metafunctions

| Metafunctions |
| ------------- |
| __index |
| __ipairs |
| __newindex |
| __pairs |


### Property Descriptions



### Function Descriptions



---

## <a href='#ElementTabSet' name='ElementTabSet'>ElementTabSet</a>

Inherits: `Element`{: .lua-type }

ElementTabSet derives from Element. The control has the following functions and properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [active_tab](#ElementTabSet-active_tab){: .lua-function } | `integer`{: .lua-type } |
| [num_tabs](#ElementTabSet-num_tabs){: .lua-function } | `integer`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [SetPanel](#ElementTabSet-SetPanel){: .lua-function }(`integer`{: .lua-type } index, `string`{: .lua-type } rml) | `nil`{: .lua-type } |
| [SetTab](#ElementTabSet-SetTab){: .lua-function }(`integer`{: .lua-type } index, `string`{: .lua-type } rml) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

####  `integer`{: .lua-type } <a href='#ElementTabSet-active_tab' name='ElementTabSet-active_tab'>active_tab</a>{: .lua-function }

Index of the active panel.

####  `integer`{: .lua-type } <a href='#ElementTabSet-num_tabs' name='ElementTabSet-num_tabs'>num_tabs</a>{: .lua-function }

The number of tabs in the tab set. Read-only.



### Function Descriptions

#### `nil`{: .lua-type} <a href='#ElementTabSet-SetPanel' name='ElementTabSet-SetPanel'>SetPanel</a>{: .lua-function }(`integer`{: .lua-type } index, `string`{: .lua-type } rml)

Sets the contents of a panel to the RML content rml. If index is out-of-bounds, a new panel will be added at the end.

#### `nil`{: .lua-type} <a href='#ElementTabSet-SetTab' name='ElementTabSet-SetTab'>SetTab</a>{: .lua-function }(`integer`{: .lua-type } index, `string`{: .lua-type } rml)

Sets the contents of a tab to the RML content rml. If index is out-of-bounds, a new tab will be added at the end.



---

## <a href='#ElementText' name='ElementText'>ElementText</a>

Inherits: `Element`{: .lua-type }



### Properties

| Name | Type |
| ------------ | ---- |
| [text](#ElementText-text){: .lua-function } | `string`{: .lua-type } |


### Functions




### Metafunctions




### Property Descriptions

####  `string`{: .lua-type } <a href='#ElementText-text' name='ElementText-text'>text</a>{: .lua-function }





### Function Descriptions



---

## <a href='#Event' name='Event'>Event</a>

Inherits: `nil`{: .lua-type }

The Event class has no constructor; it is generated internally. It has the following functions and properties:

### Properties

| Name | Type |
| ------------ | ---- |
| [current_element](#Event-current_element){: .lua-function } | `Element`{: .lua-type } |
| [parameters](#Event-parameters){: .lua-function } | `EventParametersProxy`{: .lua-type } |
| [target_element](#Event-target_element){: .lua-function } | `Element`{: .lua-type } |
| [type](#Event-type){: .lua-function } | `string`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [StopPropagation](#Event-StopPropagation){: .lua-function }() | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

####  `Element`{: .lua-type } <a href='#Event-current_element' name='Event-current_element'>current_element</a>{: .lua-function }

The element the event has propagated to. Read-only.

####  `EventParametersProxy`{: .lua-type } <a href='#Event-parameters' name='Event-parameters'>parameters</a>{: .lua-function }

A dictionary like object containing all the parameters in the event.

####  `Element`{: .lua-type } <a href='#Event-target_element' name='Event-target_element'>target_element</a>{: .lua-function }

The element the event was originally targeted at. Read-only.

####  `string`{: .lua-type } <a href='#Event-type' name='Event-type'>type</a>{: .lua-function }

The string name of the event. Read-only.



### Function Descriptions

#### `nil`{: .lua-type} <a href='#Event-StopPropagation' name='Event-StopPropagation'>StopPropagation</a>{: .lua-function }()

Stops the propagation of the event through the event cycle, if allowed.



---

## <a href='#EventParametersProxy' name='EventParametersProxy'>EventParametersProxy</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions




### Metafunctions

| Metafunctions |
| ------------- |
| __index |
| __ipairs |
| __pairs |


### Property Descriptions



### Function Descriptions



---

## <a href='#GlobalLuaFunctions' name='GlobalLuaFunctions'>GlobalLuaFunctions</a>

Inherits: `nil`{: .lua-type }



### Properties

| Name | Type |
| ------------ | ---- |
| [ipairsaux](#GlobalLuaFunctions-ipairsaux){: .lua-function } | `nil`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [LuaPrint](#GlobalLuaFunctions-LuaPrint){: .lua-function }(`...` output) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

#### `nil`{: .lua-type } <a href='#GlobalLuaFunctions-ipairsaux' name='GlobalLuaFunctions-ipairsaux'>ipairsaux</a>{: .lua-function }





### Function Descriptions

#### `nil`{: .lua-type} <a href='#GlobalLuaFunctions-LuaPrint' name='GlobalLuaFunctions-LuaPrint'>LuaPrint</a>{: .lua-function }(`...` output)

Print all the values that are passed in as arguments

---

## <a href='#Log' name='Log'>Log</a>

Inherits: `nil`{: .lua-type }

Log messages through RmlUi.

### Properties

| Name | Type |
| ------------ | ---- |
| [logtype](#Log-logtype){: .lua-function } | `table`{: .lua-type } |

### Functions

| Name | Return Type |
| ------------ | ---- |
| [Message](#Log-Message){: .lua-function }(`Log.logtype`{: .lua-type } type, `string`{: .lua-type } str) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

#### `table`{: .lua-type } <a href='#Log-logtype' name='Log-logtype'>logtype</a>{: .lua-function }

Enum table for specifying the type of log.

* `Log.logtype.always`
* `Log.logtype.error`
* `Log.logtype.warning`
* `Log.logtype.info`
* `Log.logtype.debug`

### Function Descriptions

#### `nil`{: .lua-type} <a href='#Message' name='Message'>Message</a>{: .lua-function }(`Log.logtype`{: .lua-type } type, `string`{: .lua-type } str)

Log a message with a type.

---

## <a href='#rmlui' name='rmlui'>rmlui</a>

Inherits: `nil`{: .lua-type }

`rmlui` exposes some general RmlUi functionality globally in Lua. Access with the global table `rmlui`.

### Properties

| Name | Type |
| ------------ | ---- |
| [contexts](#LuaRmlUi-contexts){: .lua-function } | `RmlUiContextsProxy`{: .lua-type } |
| [key_identifier](#LuaRmlUi-key_identifier){: .lua-function } | `table`{: .lua-type } |
| [key_modifier](#LuaRmlUi-key_modifier){: .lua-function } | `table`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [CreateContext](#LuaRmlUi-CreateContext){: .lua-function }(`string`{: .lua-type } name, `Vector2i`{: .lua-type } dimensions) | `nil`{: .lua-type }<br>`Context`{: .lua-type }<br> |
| [LoadFontFace](#LuaRmlUi-LoadFontFace){: .lua-function }(`string`{: .lua-type } path) | `boolean`{: .lua-type }<br> |
| [RegisterTag](#LuaRmlUi-RegisterTag){: .lua-function }(`string`{: .lua-type } tag) | `nil`{: .lua-type } |


### Metafunctions




### Property Descriptions

####  `RmlUiContextsProxy`{: .lua-type } <a href='#LuaRmlUi-contexts' name='LuaRmlUi-contexts'>contexts</a>{: .lua-function }

Table of active contexts indexable with integers and context name strings.

#### `table`{: .lua-type } <a href='#LuaRmlUi-key_identifier' name='LuaRmlUi-key_identifier'>key_identifier</a>{: .lua-function }

Enum containing all input key identifiers.

#### `table`{: .lua-type } <a href='#LuaRmlUi-key_modifier' name='LuaRmlUi-key_modifier'>key_modifier</a>{: .lua-function }

Enum containing all input key modifiers.

### Function Descriptions

####  `Context`{: .lua-type }, `Context`{: .lua-type } <a href='#LuaRmlUi-CreateContext' name='LuaRmlUi-CreateContext'>CreateContext</a>{: .lua-function }(`string`{: .lua-type } name, `Vector2i`{: .lua-type } dimensions)

Create RmlUi context with specified `dimensions`.

####  `boolean`{: .lua-type } <a href='#LuaRmlUi-LoadFontFace' name='LuaRmlUi-LoadFontFace'>LoadFontFace</a>{: .lua-function }(`string`{: .lua-type } path)

Load font face at `path`

#### `nil`{: .lua-type} <a href='#LuaRmlUi-RegisterTag' name='LuaRmlUi-RegisterTag'>RegisterTag</a>{: .lua-function }(`string`{: .lua-type } tag)

Register tag to element instancer.

---

## <a href='#RmlUiContextsProxy' name='RmlUiContextsProxy'>RmlUiContextsProxy</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions




### Metafunctions

| Metafunctions |
| ------------- |
| __index |
| __ipairs |
| __pairs |


### Property Descriptions



### Function Descriptions



---

## <a href='#SelectOptionsProxy' name='SelectOptionsProxy'>SelectOptionsProxy</a>

Inherits: `nil`{: .lua-type }



### Properties




### Functions




### Metafunctions

| Metafunctions |
| ------------- |
| __index |
| __ipairs |
| __pairs |


### Property Descriptions



### Function Descriptions



---

## <a href='#Vector2f' name='Vector2f'>Vector2f</a>

Inherits: `nil`{: .lua-type }

Constructs a two-dimensional floating-point vector.

### Properties

| Name | Type |
| ------------ | ---- |
| [magnitude](#Vector2f-magnitude){: .lua-function } | `number`{: .lua-type } |
| [x](#Vector2f-x){: .lua-function } | `number`{: .lua-type } |
| [y](#Vector2f-y){: .lua-function } | `number`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [DotProduct](#Vector2f-DotProduct){: .lua-function }(`Vector2f`{: .lua-type } other) | `number`{: .lua-type }<br> |
| [Normalise](#Vector2f-Normalise){: .lua-function }() | `Vector2f`{: .lua-type }<br> |
| [Rotate](#Vector2f-Rotate){: .lua-function }(`number`{: .lua-type } angle) | `Vector2f`{: .lua-type }<br> |
| [new](#Vector2f-new){: .lua-function }(`number`{: .lua-type } x, `number`{: .lua-type } y) | `Vector2f`{: .lua-type} |


### Metafunctions

| Metafunctions |
| ------------- |
| __add |
| __div |
| __eq |
| __mul |
| __sub |


### Property Descriptions

####  `number`{: .lua-type } <a href='#Vector2f-magnitude' name='Vector2f-magnitude'>magnitude</a>{: .lua-function }



####  `number`{: .lua-type } <a href='#Vector2f-x' name='Vector2f-x'>x</a>{: .lua-function }



####  `number`{: .lua-type } <a href='#Vector2f-y' name='Vector2f-y'>y</a>{: .lua-function }





### Function Descriptions

####  `number`{: .lua-type } <a href='#Vector2f-DotProduct' name='Vector2f-DotProduct'>DotProduct</a>{: .lua-function }(`Vector2f`{: .lua-type } other)



####  `Vector2f`{: .lua-type } <a href='#Vector2f-Normalise' name='Vector2f-Normalise'>Normalise</a>{: .lua-function }()



####  `Vector2f`{: .lua-type } <a href='#Vector2f-Rotate' name='Vector2f-Rotate'>Rotate</a>{: .lua-function }(`number`{: .lua-type } angle)



#### `Vector2f`{: .lua-type} <a href='#Vector2f-new' name='Vector2f-new'>new</a>{: .lua-function }(`number`{: .lua-type } x, `number`{: .lua-type } y)





---

## <a href='#Vector2i' name='Vector2i'>Vector2i</a>

Inherits: `nil`{: .lua-type }

Constructs a two-dimensional integral vector.

### Properties

| Name | Type |
| ------------ | ---- |
| [magnitude](#Vector2i-magnitude){: .lua-function } | `number`{: .lua-type } |
| [x](#Vector2i-x){: .lua-function } | `integer`{: .lua-type } |
| [y](#Vector2i-y){: .lua-function } | `integer`{: .lua-type } |


### Functions

| Name | Return Type |
| ------------ | ---- |
| [new](#Vector2i-new){: .lua-function }(`integer`{: .lua-type } x, `integer`{: .lua-type } y) | `Vector2i`{: .lua-type} |


### Metafunctions

| Metafunctions |
| ------------- |
| __add |
| __div |
| __eq |
| __mul |
| __sub |


### Property Descriptions

####  `number`{: .lua-type } <a href='#Vector2i-magnitude' name='Vector2i-magnitude'>magnitude</a>{: .lua-function }



####  `integer`{: .lua-type } <a href='#Vector2i-x' name='Vector2i-x'>x</a>{: .lua-function }



####  `integer`{: .lua-type } <a href='#Vector2i-y' name='Vector2i-y'>y</a>{: .lua-function }





### Function Descriptions

#### `Vector2i`{: .lua-type} <a href='#Vector2i-new' name='Vector2i-new'>new</a>{: .lua-function }(`integer`{: .lua-type } x, `integer`{: .lua-type } y)





---