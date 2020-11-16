---
UID: NS:directml.DML_AVERAGE_POOLING_OPERATOR_DESC
title: DML_AVERAGE_POOLING_OPERATOR_DESC
description: Averages values across the elements within the sliding window over the input tensor.
helpviewer_keywords: ["DML_AVERAGE_POOLING_OPERATOR_DESC","DML_AVERAGE_POOLING_OPERATOR_DESC structure","direct3d12.dml_average_pooling_operator_desc","directml/DML_AVERAGE_POOLING_OPERATOR_DESC"]
old-location: direct3d12\dml_average_pooling_operator_desc.htm
tech.root: directml
ms.assetid: 343A104A-208F-4AB9-A1E7-7EC83FB84AC5
ms.date: 10/28/2020
ms.keywords: DML_AVERAGE_POOLING_OPERATOR_DESC, DML_AVERAGE_POOLING_OPERATOR_DESC structure, direct3d12.dml_average_pooling_operator_desc, directml/DML_AVERAGE_POOLING_OPERATOR_DESC
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
 - DML_AVERAGE_POOLING_OPERATOR_DESC
 - directml/DML_AVERAGE_POOLING_OPERATOR_DESC
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
 - DML_AVERAGE_POOLING_OPERATOR_DESC
---

## -description

Averages values across the elements within the sliding window over the input tensor.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An input tensor of *Sizes* `{ BatchCount, ChannelCount, Height, Width }` for 4D, and `{ BatchCount, ChannelCount, Depth, Height, Weight }` for 5D.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A description of the output tensor. The sizes of the output tensor can be computed as follows.

```cpp
OutputTensor->Sizes[0] = InputTensor->Sizes[0];
OutputTensor->Sizes[1] = InputTensor->Sizes[1];

for (UINT i = 0; i < DimensionCount; ++i) {
    UINT PaddedSize = InputTensor->Sizes[i + 2] + StartPadding[i] + EndPadding[i];
    OutputTensor->Sizes[i + 2] = (PaddedSize - WindowSizes[i]) / Strides[i] + 1;
}
```

### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of spatial dimensions of the input tensor *InputTensor*, which also corresponds to the number of dimensions of the sliding window *WindowSize*. This value also determines the size of the *Strides*, *StartPadding*, and *EndPadding* arrays. It should be set to 2 when *InputTensor* is 4D, and 3 when it's a 5D tensor.

### -field Strides

Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***

The strides for the sliding window dimensions of sizes `{ Height, Width }` when the *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.

### -field WindowSize

Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***

The dimensions of the sliding window in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.

### -field StartPadding

Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***

The number of padding elements to be applied to the beginning of each spatial dimension of the input tensor *InputTensor*. The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.

### -field EndPadding

Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***

The number of padding elements to be applied to the end of each spatial dimension of the input tensor *InputTensor*. The values are in `{ Height, Width }` when *DimensionCount* is set to 2, or `{ Depth, Height, Width }` when set to 3.

### -field IncludePadding

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Indicates whether to include the padding elements around the spatial edges when calculating the average value across all elements within the sliding window. When the value is set to **FALSE**, the padding elements are not counted as part of the divisor value of the averaging calculation.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType* and *DimensionCount*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16 |
