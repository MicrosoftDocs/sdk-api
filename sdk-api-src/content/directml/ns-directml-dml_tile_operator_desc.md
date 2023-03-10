---
UID: NS:directml.DML_TILE_OPERATOR_DESC
title: DML_TILE_OPERATOR_DESC
description: Constructs an output tensor by tiling the input tensor. The elements in each dimension of the input tensor are repeated by a multiple in the *Repeats* array.
helpviewer_keywords: ["DML_TILE_OPERATOR_DESC","DML_TILE_OPERATOR_DESC structure","direct3d12.dml_tile_operator_desc","directml/DML_TILE_OPERATOR_DESC"]
old-location: direct3d12\dml_tile_operator_desc.htm
tech.root: directml
ms.assetid: 98D39D8F-4165-4642-B139-EE7417403FCA
ms.date: 11/04/2020
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
 - DML_TILE_OPERATOR_DESC
 - directml/DML_TILE_OPERATOR_DESC
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
 - DML_TILE_OPERATOR_DESC
---

## -description

Constructs an output tensor by tiling the input tensor. The elements in each dimension of the input tensor are repeated by a multiple in the *Repeats* array.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to read from, which contains the elements to be tiled.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write to, which will hold the tiled output. For each dimension `i` in `[0, InputTensor.DimensionCount-1]`, the output size is calculated as `OutputTensor.Sizes[i] = InputTensor.Sizes[i] * Repeats[i]`. This tensor must have the same *DimensionCount* as the input tensor.

### -field RepeatsCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the *Repeats* array. This value must be the same as the *InputTensor.DimensionCount*.

### -field Repeats

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

Each value in this array corresponds to one of the input tensor's dimensions (in order). Each value is the number of tiled copies to make of that dimension. Values must be larger than 0.

## Examples

```
RepeatsCount: 4
Repeats: {1, 1, 3, 3}

InputTensor: (Sizes:{1, 1, 2, 3}, DataType:FLOAT32)
[[[[1, 2, 3]
   [4, 5, 6]]]]

InputTensor: (Sizes:{1, 1, 6, 9}, DataType:FLOAT32)
[[[[1, 2, 3, 1, 2, 3, 1, 2, 3]
   [4, 5, 6, 4, 5, 6, 4, 5, 6] 
   [1, 2, 3, 1, 2, 3, 1, 2, 3] 
   [4, 5, 6, 4, 5, 6, 4, 5, 6] 
   [1, 2, 3, 1, 2, 3, 1, 2, 3] 
   [4, 5, 6, 4, 5, 6, 4, 5, 6]]]]
```

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*.

## Tensor support

### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_1 and above

| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above

| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above

| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
