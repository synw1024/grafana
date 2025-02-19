---
keywords:
  - grafana
  - schema
title: NodeGraphPanelCfg kind
---
> Both documentation generation and kinds schemas are in active development and subject to change without prior notice.

# NodeGraphPanelCfg kind

## Maturity: experimental
## Version: 0.0

## Properties

| Property       | Type                    | Required | Description |
|----------------|-------------------------|----------|-------------|
| `ArcOption`    | [object](#arcoption)    | **Yes**  |             |
| `EdgeOptions`  | [object](#edgeoptions)  | **Yes**  |             |
| `NodeOptions`  | [object](#nodeoptions)  | **Yes**  |             |
| `PanelOptions` | [object](#paneloptions) | **Yes**  |             |

## ArcOption

### Properties

| Property | Type   | Required | Description                                                                                         |
|----------|--------|----------|-----------------------------------------------------------------------------------------------------|
| `color`  | string | No       | The color of the arc.                                                                               |
| `field`  | string | No       | Field from which to get the value. Values should be less than 1, representing fraction of a circle. |

## EdgeOptions

### Properties

| Property            | Type   | Required | Description                                                                 |
|---------------------|--------|----------|-----------------------------------------------------------------------------|
| `mainStatUnit`      | string | No       | Unit for the main stat to override what ever is set in the data frame.      |
| `secondaryStatUnit` | string | No       | Unit for the secondary stat to override what ever is set in the data frame. |

## NodeOptions

### Properties

| Property            | Type                      | Required | Description                                                                             |
|---------------------|---------------------------|----------|-----------------------------------------------------------------------------------------|
| `arcs`              | [ArcOption](#arcoption)[] | No       | Define which fields are shown as part of the node arc (colored circle around the node). |
| `mainStatUnit`      | string                    | No       | Unit for the main stat to override what ever is set in the data frame.                  |
| `secondaryStatUnit` | string                    | No       | Unit for the secondary stat to override what ever is set in the data frame.             |

### ArcOption

#### Properties

| Property | Type   | Required | Description                                                                                         |
|----------|--------|----------|-----------------------------------------------------------------------------------------------------|
| `color`  | string | No       | The color of the arc.                                                                               |
| `field`  | string | No       | Field from which to get the value. Values should be less than 1, representing fraction of a circle. |

## PanelOptions

### Properties

| Property | Type                        | Required | Description |
|----------|-----------------------------|----------|-------------|
| `edges`  | [EdgeOptions](#edgeoptions) | No       |             |
| `nodes`  | [NodeOptions](#nodeoptions) | No       |             |

### EdgeOptions

#### Properties

| Property            | Type   | Required | Description                                                                 |
|---------------------|--------|----------|-----------------------------------------------------------------------------|
| `mainStatUnit`      | string | No       | Unit for the main stat to override what ever is set in the data frame.      |
| `secondaryStatUnit` | string | No       | Unit for the secondary stat to override what ever is set in the data frame. |

### NodeOptions

#### Properties

| Property            | Type                      | Required | Description                                                                             |
|---------------------|---------------------------|----------|-----------------------------------------------------------------------------------------|
| `arcs`              | [ArcOption](#arcoption)[] | No       | Define which fields are shown as part of the node arc (colored circle around the node). |
| `mainStatUnit`      | string                    | No       | Unit for the main stat to override what ever is set in the data frame.                  |
| `secondaryStatUnit` | string                    | No       | Unit for the secondary stat to override what ever is set in the data frame.             |

#### ArcOption

##### Properties

| Property | Type   | Required | Description                                                                                         |
|----------|--------|----------|-----------------------------------------------------------------------------------------------------|
| `color`  | string | No       | The color of the arc.                                                                               |
| `field`  | string | No       | Field from which to get the value. Values should be less than 1, representing fraction of a circle. |


