---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
description: Performs a mean variance normalization function on the input tensor. This operator will calculate the mean and variance of the input tensor to perform normalization. (DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC)
helpviewer_keywords: ["DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC","DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC structure","direct3d12.dml_mean_variance_normalization_operator_desc","directml/DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC"]
old-location: direct3d12\dml_mean_variance_normalization_operator_desc.htm
tech.root: directml
ms.assetid: AF70005F-BDBB-45C9-9066-70A574D5BC0E
ms.date: 05/02/2023
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
 - DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
 - directml/DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
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
 - DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC
---

## -description

Performs a mean variance normalization function on the input tensor. This operator will calculate the mean and variance of the input tensor to perform normalization. This operator performs the following computation.

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Input data. This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.

### -field ScaleTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the Scale data. This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`. Any dimension can be replaced with 1 to broadcast in that dimension. If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_5_2**, then this tensor is required if *BiasTensor* is present. If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_5_2**, then this tensor can be null regardless of the value of *BiasTensor*.

### -field BiasTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the bias data. This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`. Any dimension can be replaced with 1 to broadcast in that dimension. If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_5_2**, then this tensor is required if *ScaleTensor* is present. If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_5_2**, then this tensor can be null regardless of the value of *ScaleTensor*.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the results to. This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.

### -field CrossChannel

Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

When **TRUE**, the MeanVariance layer includes channels in the Mean and Variance calculations, meaning they are normalized across axes `{ChannelCount, Height, Width}`. When **FALSE**, Mean and Variance calculations are normalized across axes `{Height, Width}` with each channel being independent.

### -field NormalizeVariance

Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

**TRUE** if the Normalization layer includes Variance in the normalization calculation. Otherwise, **FALSE**. If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.

### -field Epsilon

Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b>

The epsilon value to use to avoid division by zero. A value of 0.00001 is recommended as default.

### -field FusedActivation

Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An optional fused activation layer to apply after the normalization. For more info, see [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations).

## -remarks
A newer version of this operator, [DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization1_operator_desc), was introduced in `DML_FEATURE_LEVEL_2_1`.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *InputTensor* and *OutputTensor* must have the same *Sizes*.
* *BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.

## Tensor support
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { BatchCount, ChannelCount, Height, Width } | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Optional input | { ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth } | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Optional input | { BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { BatchCount, ChannelCount, Height, Width } | 4 | FLOAT32, FLOAT16 |

## -see-also

* [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations)
