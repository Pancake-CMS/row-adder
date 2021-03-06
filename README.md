# row-adder
A web component that manages the user component that was added via `css-grid`. This component lets the user to edit __css grid__ properties as well __component specific properties__ that it will need in a particular context.

## Installation

```shell
bower install --save pancake-cms-row-adder
```

## Attributes

| name |  type | description | example value |
|------|-------|-------------|---------------|
| el-name | String | The name of the component that needs to be rendered by `row-adder` element | `demo-el` or `registration-card` |
| in-edit-mode | Boolean | Are we rendering `row-adder` in edit mode or not. This element shows a lot of options when in edit mode | `true` or `false` |
| component-properties | Object | This is the main part of `row-adder` element. Its main purpose is to let users modify the properties given in this object. | Please refer the section __component-properties__ for more information on its structure |

## Events

The element triggers a `component-modified` event when anything changes in its properties. This happens when the user changes anything in the properties dialog.

## component-properties

The most basic example of this object is as follows

```javascript
[
    {
        "name" : "display",
        "value" : [
            {
                "description" : "The start column location of this component",
                "name" : "gridColumnStart",
                "type" : "text",
                "value" : "1"
            }, {
                "description" : "The end column location of this component",
                "name" : "gridColumnEnd",
                "type" : "text",
                "value" : "12"
            }, {
                "description" : "The start row location of this component",
                "name" : "gridRowStart",
                "type" : "text",
                "value" : ""
            }, {
                "description" : "The end row location of this component",
                "name" : "gridRowEnd",
                "type" : "text",
                "value" : ""
            }
        ]
    },
    {
        name: 'Component Properties',
        value: [
            {
                name: 'productName',
                value: 'Some Product Name',
                type: 'text',
                description: 'The name of the product that needs to be displayed'
            }
        ]
    }
]
```