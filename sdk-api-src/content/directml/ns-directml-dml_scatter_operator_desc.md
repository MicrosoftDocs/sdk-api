---
UID: NS:directml.DML_SCATTER_OPERATOR_DESC
title: DML_SCATTER_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor. (DML_SCATTER_OPERATOR_DESC)
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
 - DML_SCATTER_OPERATOR_DESC
f1_keywords:
 - DML_SCATTER_OPERATOR_DESC
 - directml/DML_SCATTER_OPERATOR_DESC
---

## -description

Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor. This operator performs the following pseudocode.

```
output = input
output[index[i, j, k, ...], j, k, ...] = updates[i, j, k, ...] // if axis == 0
output[i, index[i, j, k, ...], k, ...] = updates[i, j, k, ...] // if axis == 1
output[i, j, index[i, j, k, ...], ...] = updates[i, j, k, ...] // if axis == 2
...
```

If two output element indices overlap (which is invalid), then there's no guarantee of which last write wins.

**DML_SCATTER_OPERATOR_DESC** is the inverse of [DML_GATHER_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_operator_desc).

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to read from.

### -field IndicesTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the indices into the output tensor. The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.

Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor. Negative indices are interpreted as being relative to the end of the axis dimension. For example, an index of -1 refers to the last element along that dimension.

### -field UpdatesTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the new values to replace the existing input values at the corresponding indices. The *Sizes* of this tensor must match *IndicesTensor.Sizes*. The *DataType* must match *InputTensor.DataType*.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. The *Sizes* and *DataType* of this tensor must match *InputTensor*.

### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The axis dimension to use for indexing in *OutputTensor*, ranging `[0, OutputTensor.DimensionCount)`.

## Examples

### Example 1. 1D scatter

```
Axis: 0

InputTensor: (Sizes:{5}, DataType:FLOAT32)
    [0,1,2,3,4]

IndicesTensor: (Sizes:{4}, DataType:UINT32)
    [3,1,3,0]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [5,6,7,8]

// output = input
// output[indices[x]] = updates[x]
OutputTensor: (Sizes:{5}, DataType:FLOAT32)
    [8,6,2,7,4]
```

### Example 2. 2D scatter

```
Axis: 0

InputTensor: (Sizes:{2,3}, DataType:FLOAT32)
    [[0.0, 0.0, 0.0],
     [0.0, 0.0, 0.0],
     [0.0, 0.0, 0.0]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 0, 2],
     [0, 2, 1]]

UpdatesTensor: (Sizes:{2,3}, DataType:FLOAT32)
    [[10, 11, 12],
     [20, 21, 22]]

// output = input
// output[indices[y, x], x] = updates[y, x]
OutputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[20, 11,  0],
     [10,  0, 22],
     [ 0, 21, 12]]
```

## -remarks

**DML_SCATTER_OPERATOR_DESC** has been more properly aliased to the name **DML_SCATTER_ELEMENTS_OPERATOR_DESC** as the proper counterpart to [DML_GATHER_ELEMENTS_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_elements_operator_desc). This is because **DML_SCATTER_OPERATOR_DESC** was not really symmetric to [DML_GATHER_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_operator_desc).

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *IndicesTensor*, *InputTensor*, *OutputTensor*, and *UpdatesTensor* must have the same *DimensionCount*.
* *InputTensor*, *OutputTensor*, and *UpdatesTensor* must have the same *DataType*.

## Tensor support

### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 1 to 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Input | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 1 to 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 4 | UINT32 |
| UpdatesTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| IndicesTensor | Input | 4 | UINT32 |
| UpdatesTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also
