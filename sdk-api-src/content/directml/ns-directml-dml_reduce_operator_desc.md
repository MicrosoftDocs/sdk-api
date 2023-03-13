---
UID: NS:directml.DML_REDUCE_OPERATOR_DESC
title: DML_REDUCE_OPERATOR_DESC
description: Outputs the reduction of elements (sum, product, minimum, and so on) within one or more dimensions of the input tensor.
helpviewer_keywords: ["DML_REDUCE_OPERATOR_DESC","DML_REDUCE_OPERATOR_DESC structure","direct3d12.dml_reduce_operator_desc","directml/DML_REDUCE_OPERATOR_DESC"]
old-location: direct3d12\dml_reduce_operator_desc.htm
tech.root: directml
ms.assetid: 6C390A1A-7AA3-4B24-8DC7-A34E6FBE6320
ms.date: 01/19/2022
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_REDUCE_OPERATOR_DESC
 - directml/DML_REDUCE_OPERATOR_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_REDUCE_OPERATOR_DESC
---

## -description

Outputs the reduction of elements (sum, product, minimum, and so on) within one or more dimensions of the input tensor.

Each output element is the result of applying a reduction function on a subset of the input tensor. A reduction function, such as *sum*, maps `N` input elements to a single output element. The input elements involved in each reduction are determined by the provided input axes: `N` is equal to the product of the sizes of the reduced axes. If all input axes are specified, then the operator performs a reduction on the entire input tensor and produces a single output element.

## -struct-fields

### -field Function

Type: [**DML_REDUCE_FUNCTION**](/windows/win32/api/directml/ne-directml-dml_reduce_function)

Specifies the reduction function to apply to the input.

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. Each output element is the result of a reduction on a subset of elements from the *InputTensor*.

- *DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).
- *Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.

### -field AxisCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of axes to reduce. This field determines the size of the *Axes* array.

### -field Axes

Type: \_Field\_size\_(AxisCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

The axes along which to reduce. Values must be in the range `[0, InputTensor.DimensionCount - 1]`.

## Examples

The following examples all use this same two-dimensional input tensor.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 4, 2]]
```

### Example 1. Applying *sum* to columns

```
Function: DML_REDUCE_FUNCTION_SUM
AxisCount: 1
Axes: {0}
OutputTensor: (Sizes:{1, 3}, DataType:FLOAT32)
[[6,  // sum({1, 3, 2})
  6,  // sum({2, 0, 4})
  9]] // sum({3, 4, 2})
```

### Example 2. Applying *sum* to rows

```
Function: DML_REDUCE_FUNCTION_SUM
AxisCount: 1
Axes: {1}
OutputTensor: (Sizes:{3, 1}, DataType:FLOAT32)
[[6], // sum({1, 2, 3})
 [7], // sum({3, 0, 4})
 [8]] // sum({2, 4, 2})
```

### Example 3.Applying *sum* to all axes (the entire tensor)

```
Function: DML_REDUCE_FUNCTION_SUM
AxisCount: 2
Axes: {0, 1}
OutputTensor: (Sizes:{1, 1}, DataType:FLOAT32)
[[21]]  // sum({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* The input and output tensor data types must match except when using the ARGMAX and ARGMIN functions, which always output an integral data type.
* The output sizes must be the same as the input sizes except for the reduced axes, which must be 1.

## Tensor support according to function
### ARGMIN and ARGMAX
##### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | INT64, INT32, UINT64, UINT32 |

#### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | INT64, INT32, UINT64, UINT32 |

#### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | UINT32 |

#### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | UINT32 |

### AVERAGE, L2, LOG_SUM, and LOG_SUM_EXP
##### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

##### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

### L1 and SUM_SQUARE
##### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, UINT64, UINT32 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, UINT64, UINT32 |

#### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

#### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

### MIN and MAX
##### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

#### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

#### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, UINT32 |

#### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

### MULTIPLY and SUM
##### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, UINT64, UINT32 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, UINT64, UINT32 |

#### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, UINT32 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, UINT32 |

#### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, UINT32 |

#### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also

Feature level 3_0 introduced these stand-alone operators that supersede the functionality available with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function) and **DML_REDUCE_FUNCTION_ARGMIN**.

* [DML_ARGMAX_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_argmax_operator_desc)
* [DML_ARGMIN_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_argmin_operator_desc)
