---
UID: NS:directml.DML_BATCH_NORMALIZATION_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_OPERATOR_DESC
description: Performs a batch normalization on the input.
helpviewer_keywords: ["DML_BATCH_NORMALIZATION_OPERATOR_DESC","DML_BATCH_NORMALIZATION_OPERATOR_DESC structure","direct3d12.dml_batch_normalization_operator_desc","directml/DML_BATCH_NORMALIZATION_OPERATOR_DESC"]
old-location: direct3d12\dml_batch_normalization_operator_desc.htm
tech.root: directml
ms.assetid: 6589B3EF-1DB9-4E52-B0D2-31C94A725F07
ms.date: 11/24/2020
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
 - DML_BATCH_NORMALIZATION_OPERATOR_DESC
 - directml/DML_BATCH_NORMALIZATION_OPERATOR_DESC
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
 - DML_BATCH_NORMALIZATION_OPERATOR_DESC
---

## -description

Performs a batch normalization on the input. This operator performs the following computation: `Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias)`.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Input data. This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.

### -field MeanTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Mean data. This tensor's dimensions should be `{ MeanBatchCount, ChannelCount, MeanHeight, MeanWidth }`. The dimensions MeanBatchCount, MeanHeight, and MeanWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.

### -field VarianceTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Variance data. This tensor's dimensions should be `{ VarianceBatchCount, ChannelCount, VarianceHeight, VarianceWidth }`. The dimensions VarianceBatchCount, VarianceHeight, and VarianceWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.

### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Scale data. This tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`. The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.

### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Bias data. This tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`. The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the results to. This tensor's dimensions should match *InputTensor*.

### -field Spatial

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

**TRUE** to specify that locations are spatial, otherwise **FALSE**. Setting this to **FALSE** will require the Width and Height dimensions of *MeanTensor* and *VarianceTensor* to not be broadcast.

### -field Epsilon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The epsilon value to use to avoid division by zero.

### -field FusedActivation

Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An optional fused activation layer to apply after the normalization.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *InputTensor* and *OutputTensor* must have the same *Sizes*.
* *BiasTensor*, *InputTensor*, *MeanTensor*, *OutputTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType*.

## Tensor support
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { BatchCount, ChannelCount, Height, Width } | 4 | FLOAT32, FLOAT16 |
| MeanTensor | Input | { MeanBatchCount, ChannelCount, MeanHeight, MeanWidth } | 4 | FLOAT32, FLOAT16 |
| VarianceTensor | Input | { VarianceBatchCount, ChannelCount, VarianceHeight, VarianceWidth } | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Input | { ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth } | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Input | { BiasBatchCount, ChannelCount, BiasHeight, BiasWidth } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { BatchCount, ChannelCount, Height, Width } | 4 | FLOAT32, FLOAT16 |

## -see-also
[Using fused operators for improved performance](/windows/win32/direct3d12/dml-fused-activations)
