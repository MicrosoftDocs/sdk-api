---
UID: NS:directml.DML_PADDING_OPERATOR_DESC
title: DML_PADDING_OPERATOR_DESC
description: Inflates the input tensor with constant or mirrored values on the edges, and writes the result to the output.
helpviewer_keywords: ["DML_PADDING_OPERATOR_DESC","DML_PADDING_OPERATOR_DESC structure","direct3d12.dml_padding_operator_desc","directml/DML_PADDING_OPERATOR_DESC"]
old-location: direct3d12\dml_padding_operator_desc.htm
tech.root: directml
ms.assetid: 0CC96A3F-12DF-4577-AFDD-356BC0D42C64
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
 - DML_PADDING_OPERATOR_DESC
 - directml/DML_PADDING_OPERATOR_DESC
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
 - DML_PADDING_OPERATOR_DESC
---

## -description

Inflates the input tensor with constant or mirrored values on the edges, and writes the result to the output.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the input data.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the output data. For each dimension `i`, `OutputTensor.Sizes[i] = InputTensor.Sizes[i] + StartPadding[i] + EndPadding[i]`.

### -field PaddingMode

Type: [DML_PADDING_MODE](/windows/win32/api/directml/ne-directml-dml_padding_mode)

The padding mode to use when filling the padding regions.

- **DML_PADDING_MODE_CONSTANT**. Uses a single constant value defined by *PaddingValue* for all padding values (see **Example 1**).
- **DML_PADDING_MODE_EDGE**. For each dimension, use the edge values of that dimension for all padding values (see **Example 2**).
- **DML_PADDING_MODE_REFLECTION**. Mirror the values of the tensor as if we folded it right on the edges, which means that edges are not mirrored. Note that `StartPadding[i] >= InputTensor.Sizes[i]`, and `EndPadding[i] >= InputTensor.Sizes[i]` is valid, which means that we can mirror new padding regions periodically by folding them over previous padding regions (see **Example 3**).
- **DML_PADDING_MODE_SYMMETRIC**. Similar to **DML_PADDING_MODE_REFLECTION**, but edges are also mirrored. Note that `StartPadding[i] > InputTensor.Sizes[i]`, and `EndPadding[i] > InputTensor.Sizes[i]` is valid, which means that we can mirror new padding regions periodically by folding them over previous padding regions (see **Example 4**). **This mode was introduced in feature level `DML_FEATURE_LEVEL_3_0`**.

### -field PaddingValue

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The padding value to use when `PaddingMode == DML_PADDING_MODE_CONSTANT`. This value is ignored for other padding modes. Note that if the *DataType* of the tensors is not [DML_TENSOR_DATA_TYPE_FLOAT16](/windows/win32/api/directml/ne-directml-dml_tensor_data_type) or **DML_TENSOR_DATA_TYPE_FLOAT32**, then the value might be truncated (for example, 10.6 will become 10).

### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The size of the arrays pointed to by *StartPadding* and *EndPadding*. This value must be the same value as the dimension count of *InputTensor* and *OutputTensor*.

### -field StartPadding

Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

The sizes of the padding regions to add at the beginning of each dimension. For each dimension `i`, `StartPadding[i] = OutputTensor.Sizes[i] - InputTensor.Sizes[i] - EndPadding[i]`.

### -field EndPadding

Type: \_Field\_size\_(DimensionCount) <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

The sizes of the padding regions to add at the end of each dimension. For each dimension `i`, `EndPadding[i] = OutputTensor.Sizes[i] - InputTensor.Sizes[i] - StartPadding[i]`.

## Examples

### Example 1

```
PaddingMode: DML_PADDING_MODE_CONSTANT
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

### Example 4 (starting from `DML_FEATURE_LEVEL_3_0`)

```
PaddingMode: DML_PADDING_MODE_SYMMETRIC
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
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.

## Tensor support
### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 to 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16 |
