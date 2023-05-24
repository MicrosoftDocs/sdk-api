---
UID: NS:directml.DML_PADDING1_OPERATOR_DESC
tech.root: directml
title: DML_PADDING1_OPERATOR_DESC
ms.date: 08/12/2022
targetos: Windows
description: The DML_PADDING1_OPERATOR_DESC structure (directml.h) inflates the input tensor with constant or mirrored values on the edges, and writes the result to the output.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: directml.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - directml.h
api_name:
 - DML_PADDING1_OPERATOR_DESC
f1_keywords:
 - DML_PADDING1_OPERATOR_DESC
 - directml/DML_PADDING1_OPERATOR_DESC
dev_langs:
 - c++
helpviewer_keywords:
 - DML_PADDING1_OPERATOR_DESC
---

## -description

Inflates the input tensor with constant or mirrored values on the edges, and writes the result to the output.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the input data.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the output data. For each dimension *i*, `OutputTensor.Sizes[i] = InputTensor.Sizes[i] + StartPadding[i] + EndPadding[i]`.

### -field PaddingMode

Type: **[DML_PADDING_MODE](/windows/win32/api/directml/ne-directml-dml_padding_mode)\***

The padding mode to use when filling the padding regions.

- **DML_PADDING_MODE_CONSTANT**. Uses a single constant value defined by *PaddingValue* for all padding values (see **Example 1**).
- **DML_PADDING_MODE_EDGE**. For each dimension, use the edge values of that dimension for all padding values (see **Example 2**).
- **DML_PADDING_MODE_REFLECTION**. Mirror the values of the tensor as if we folded it right on the edges, which means that edges are not mirrored. Note that `StartPadding[i] >= InputTensor.Sizes[i]`, and `EndPadding[i] >= InputTensor.Sizes[i]` is valid, which means that we can mirror new padding regions periodically by folding them over previous padding regions (see **Example 3**).
- **DML_PADDING_MODE_SYMMETRIC**. Similar to **DML_PADDING_MODE_REFLECTION**, but edges are also mirrored. Note that `StartPadding[i] > InputTensor.Sizes[i]`, and `EndPadding[i] > InputTensor.Sizes[i]` is valid, which means that we can mirror new padding regions periodically by folding them over previous padding regions (see **Example 4**). **This mode was introduced in feature level `DML_FEATURE_LEVEL_3_0`**.

### -field PaddingValueDataType

Type: [**DML_TENSOR_DATA_TYPE**](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)

The data type of the *PaddingValue* member, which must match *OutputTensor.DataType*.

### -field PaddingValue

Type: **[DML_SCALAR_UNION](/windows/win32/api/directml/ns-directml-dml_scalar_union)**

The padding value to use when `PaddingMode == DML_PADDING_MODE_CONSTANT`, with *PaddingValueDataType* determining how to interpret the field. This value is ignored for other padding modes.

### -field DimensionCount

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The size of the arrays pointed to by *StartPadding* and *EndPadding*. This value must be the same value as the dimension count of *InputTensor* and *OutputTensor*.

### -field StartPadding

Type: \_Field\_size\_(DimensionCount) **const [UINT](/windows/desktop/winprog/windows-data-types)\***

The sizes of the padding regions to add at the beginning of each dimension. For each dimension *i*, `StartPadding[i] = OutputTensor.Sizes[i] - InputTensor.Sizes[i] - EndPadding[i]`.

### -field EndPadding

Type: \_Field\_size\_(DimensionCount) **const [UINT](/windows/desktop/winprog/windows-data-types)\***

The sizes of the padding regions to add at the end of each dimension. For each dimension *i*, `EndPadding[i] = OutputTensor.Sizes[i] - InputTensor.Sizes[i] - StartPadding[i]`.

## -remarks

## Examples

### Example 1

```
PaddingMode: DML_PADDING_MODE_CONSTANT
PaddingValueDataType: FLOAT32
PaddingValue: 9
StartPadding: {0, 0, 1, 2}
EndPadding: {0, 0, 3, 4}

InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[1, 2, 3, 4],
   [5, 6, 7, 8],
   [1, 2, 3, 4],
   [5, 6, 7, 8]]]]

OutputTensor: (Sizes:{1, 1, 8, 10}, DataType:FLOAT32)
[[[[9, 9, 9, 9, 9, 9, 9, 9, 9, 9]
   [9, 9, 1, 2, 3, 4, 9, 9, 9, 9],
   [9, 9, 5, 6, 7, 8, 9, 9, 9, 9],
   [9, 9, 1, 2, 3, 4, 9, 9, 9, 9],
   [9, 9, 5, 6, 7, 8, 9, 9, 9, 9],
   [9, 9, 9, 9, 9, 9, 9, 9, 9, 9],
   [9, 9, 9, 9, 9, 9, 9, 9, 9, 9],
   [9, 9, 9, 9, 9, 9, 9, 9, 9, 9]]]]
```

### Example 2

```
PaddingMode: DML_PADDING_MODE_EDGE
PaddingValueDataType: FLOAT32
StartPadding: {0, 0, 1, 2}
EndPadding: {0, 0, 3, 4}

InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[1, 2, 3, 4],
   [5, 6, 7, 8],
   [1, 2, 3, 4],
   [5, 6, 7, 8]]]]

OutputTensor: (Sizes:{1, 1, 8, 10}, DataType:FLOAT32)
[[[[1, 1, 1, 2, 3, 4, 4, 4, 4, 4]
   [1, 1, 1, 2, 3, 4, 4, 4, 4, 4],
   [5, 5, 5, 6, 7, 8, 8, 8, 8, 8],
   [1, 1, 1, 2, 3, 4, 4, 4, 4, 4],
   [5, 5, 5, 6, 7, 8, 8, 8, 8, 8],
   [5, 5, 5, 6, 7, 8, 8, 8, 8, 8],
   [5, 5, 5, 6, 7, 8, 8, 8, 8, 8],
   [5, 5, 5, 6, 7, 8, 8, 8, 8, 8]]]]
```

### Example 3

```
PaddingMode: DML_PADDING_MODE_REFLECTION
PaddingValueDataType: FLOAT32
StartPadding: {0, 0, 1, 2}
EndPadding: {0, 0, 3, 4}

InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[1, 2, 3, 4],
   [5, 6, 7, 8],
   [1, 2, 3, 4],
   [5, 6, 7, 8]]]]

OutputTensor: (Sizes:{1, 1, 8, 10}, DataType:FLOAT32)
[[[[7, 6, 5, 6, 7, 8, 7, 6, 5, 6]
   [3, 2, 1, 2, 3, 4, 3, 2, 1, 2],
   [7, 6, 5, 6, 7, 8, 7, 6, 5, 6],
   [3, 2, 1, 2, 3, 4, 3, 2, 1, 2],
   [7, 6, 5, 6, 7, 8, 7, 6, 5, 6],
   [3, 2, 1, 2, 3, 4, 3, 2, 1, 2],
   [7, 6, 5, 6, 7, 8, 7, 6, 5, 6],
   [3, 2, 1, 2, 3, 4, 3, 2, 1, 2]]]]
```

### Example 4 (starting from DML_FEATURE_LEVEL_3_0)

```
PaddingMode: DML_PADDING_MODE_SYMMETRIC
PaddingValueDataType: FLOAT32
StartPadding: {0, 0, 1, 2}
EndPadding: {0, 0, 3, 4}

InputTensor: (Sizes:{1, 1, 4, 4}, DataType:FLOAT32)
[[[[1, 2, 3, 4],
   [5, 6, 7, 8],
   [1, 2, 3, 4],
   [5, 6, 7, 8]]]]

OutputTensor: (Sizes:{1, 1, 8, 10}, DataType:FLOAT32)
[[[[2, 1, 1, 2, 3, 4, 4, 3, 2, 1]
   [2, 1, 1, 2, 3, 4, 4, 3, 2, 1],
   [6, 5, 5, 6, 7, 8, 8, 7, 6, 5],
   [2, 1, 1, 2, 3, 4, 4, 3, 2, 1],
   [6, 5, 5, 6, 7, 8, 8, 7, 6, 5],
   [6, 5, 5, 6, 7, 8, 8, 7, 6, 5],
   [2, 1, 1, 2, 3, 4, 4, 3, 2, 1],
   [6, 5, 5, 6, 7, 8, 8, 7, 6, 5]]]]
```

## Availability
This operator was introduced in **DML_FEATURE_LEVEL_5_0**.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

## -see-also
