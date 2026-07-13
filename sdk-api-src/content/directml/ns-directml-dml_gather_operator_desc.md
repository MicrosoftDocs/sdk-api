---
UID: NS:directml.DML_GATHER_OPERATOR_DESC
title: DML_GATHER_OPERATOR_DESC
description: Gathers elements from the input tensor along **Axis**, using **IndicesTensor** to remap indices.
helpviewer_keywords: ["DML_GATHER_OPERATOR_DESC","DML_GATHER_OPERATOR_DESC structure","direct3d12.dml_gather_operator_desc","directml/DML_GATHER_OPERATOR_DESC"]
old-location: direct3d12\dml_gather_operator_desc.htm
tech.root: directml
ms.assetid: 53F01BDE-30FF-4E15-BA1A-8D522B9DE8AF
ms.date: 10/30/2020
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
 - DML_GATHER_OPERATOR_DESC
 - directml/DML_GATHER_OPERATOR_DESC
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
 - DML_GATHER_OPERATOR_DESC
---

## -description

Gathers elements from the input tensor along **Axis**, using **IndicesTensor** to remap indices. This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices dimension count:

```
output[...] = input[..., indices[...], ...]
```

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to read from.

### -field IndicesTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the indices. The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.

Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor. Negative indices are interpreted as being relative to the end of the axis dimension. For example, an index of -1 refers to the last element along that dimension.

Invalid indices will yield incorrect outputs, but no failure will occur, and all reads will be clamped safely within the input tensor's memory.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*. The expected *OutputTensor.Sizes* are the concatenation of the *InputTensor.Sizes* leading and trailing segments split at the current *Axis* with the *IndicesTensor.Sizes* inserted between.

```
OutputTensor.Sizes = {
    InputTensor.Sizes[0..Axis],
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndexDimensions) .. IndicesTensor.DimensionCount],
    InputTensor.Sizes[(Axis+1) .. InputTensor.DimensionCount]
}
```

The dimensions are right-aligned such that any leading 1 values from the input sizes are cropped which would otherwise overflow the output *DimensionCount*.

The number of relevant dimensions in this tensor depends on *IndexDimensions* and the *original rank* of *InputTensor*. The original rank is the number of dimensions prior to any padding with leading ones. The number of relevant dimensions in the output can be computed by the *original rank* of *InputTensor* + *IndexDimensions* - 1. This value must be less than or equal to the *DimensionCount* of *OutputTensor*.

### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The axis dimension of *InputTensor* to gather on, ranging `[0, *InputTensor.DimensionCount*)`.

### -field IndexDimensions

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of actual index dimensions within the `IndicesTensor` after ignoring any irrelevant leading ones, ranging [0, `IndicesTensor.DimensionCount`). For example, given `IndicesTensor.Sizes` = `{ 1, 1, 4, 6 }` and `IndexDimensions` = 3, the actual meaningful indices are `{ 1, 4, 6 }`.

## Examples

### Example 1. 1D remapping

```
Axis: 0
IndexDimensions: 1

InputTensor: (Sizes:{4}, DataType:FLOAT32)
    [11,12,13,14]

IndicesTensor: (Sizes:{5}, DataType:UINT32)
    [3,1,3,0,2]

// output[x] = input[indices[x]]
OutputTensor: (Sizes:{5}, DataType:FLOAT32)
    [14,12,14,11,13]
```

### Example 2. 2D output, 1D indices, Axis 0, concatenate rows

```
Axis: 0
IndexDimensions: 1

InputTensor: (Sizes:{3,2}, DataType:FLOAT32)
    [[1,2], // row 0
     [3,4], // row 1
     [5,6]] // row 2

IndicesTensor: (Sizes:{1, 4}, DataType:UINT32)
    [[0,
      1,
      1,
      2]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{4,2}, DataType:FLOAT32)
    [[1,2], // input row 0
     [3,4], // input row 1
     [3,4], // input row 1
     [5,6]] // input row 2
```

### Example 3. 2D, Axis 1, swap columns

```
Axis: 1
IndexDimensions: 2

InputTensor: (Sizes:{3,2}, DataType:FLOAT32)
    [[1,2],
     [3,4],
     [5,6]]

IndicesTensor: (Sizes:{1, 2}, DataType:UINT32)
    [[1,0]]

// output[y, x] = input[y, indices[x]]
OutputTensor: (Sizes:{3,2}, DataType:FLOAT32)
    [[2,1],
     [4,3],
     [6,5]]
```

### Example 4. 2D, Axis 1, nested indices

```
Axis: 2
IndexDimensions: 2

InputTensor: (Sizes:{1, 3,3}, DataType:FLOAT32)
    [ [[1,2,3],
       [4,5,6],
       [7,8,9]] ]

IndicesTensor: (Sizes:{1, 1,2}, DataType:UINT32)
    [ [[0,2]] ]

// output[z, y, x] = input[z, indices[y, x]]
OutputTensor: (Sizes:{3,1,2}, DataType:FLOAT32)
    [[[1,3]],
     [[4,6]],
     [[7,9]]]
```

### Example 5. 2D, Axis 0, nested indices

```
Axis: 1
IndexDimensions: 2

InputTensor: (Sizes:{1, 3,2}, DataType:FLOAT32)
    [ [[1,2],
       [3,4],
       [5,6]] ]

IndicesTensor: (Sizes:{1, 2,2}, DataType:UINT32)
    [ [[0,1],
       [1,2]] ]

// output[z, y, x] = input[indices[z, y], x]
OutputTensor: (Sizes:{2,2,2}, DataType:FLOAT32)
    [[[1,2], [3,4]],
     [[3,4], [5,6]]]
```

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* `IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.
* *InputTensor* and *OutputTensor* must have the same *DataType*.

## Tensor support

### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 1 to 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Output | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 1 to 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Input | 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| IndicesTensor | Input | 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
