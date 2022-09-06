---
UID: NS:directml.DML_SPACE_TO_DEPTH_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH_OPERATOR_DESC
description: Rearranges blocks of spatial data into depth. The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.
helpviewer_keywords: ["DML_SPACE_TO_DEPTH_OPERATOR_DESC","DML_SPACE_TO_DEPTH_OPERATOR_DESC structure","direct3d12.dml_space_to_depth_operator_desc","directml/DML_SPACE_TO_DEPTH_OPERATOR_DESC"]
old-location: direct3d12\dml_space_to_depth_operator_desc.htm
tech.root: directml
ms.assetid: 759769E2-A379-4790-82AD-1B9D3B35D616
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
 - DML_SPACE_TO_DEPTH_OPERATOR_DESC
 - directml/DML_SPACE_TO_DEPTH_OPERATOR_DESC
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
 - DML_SPACE_TO_DEPTH_OPERATOR_DESC
---

## -description

Rearranges blocks of spatial data into depth. The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.

This is the inverse transformation of [DML_DEPTH_TO_SPACE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc).

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to read from. The input tensor's dimensions are `{ Batch, Channels, Height, Width }`.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to write the results to. The output tensor's dimensions are `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }`.

### -field BlockSize

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The width and height of the Blocks that are moved.

## Example

```
BlockSize: 2

InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]

OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

## -remarks

A newer version of this operator, [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth1_operator_desc), was introduced in `DML_FEATURE_LEVEL_2_1`.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*.

## Tensor support
### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16 |
