---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Performs a mean variance normalization function on the input tensor. This operator will calculate the mean and variance of the input tensor to perform normalization. (DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC)
helpviewer_keywords: ["DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC","DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure","direct3d12.dml_mean_variance_normalization1_operator_desc","directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC"]
tech.root: directml
ms.date: 05/02/2023
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
f1_keywords:
 - DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
 - directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
 - DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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

An optional tensor containing the Scale data.

If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`. The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.

If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.

If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_5_2**, then this tensor is required if *BiasTensor* is present. If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_5_2**, then this tensor can be null regardless of the value of *BiasTensor*.

### -field BiasTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the Bias data.

If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`. The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.

If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.

If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_5_2**, then this tensor is required if *ScaleTensor* is present. If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_5_2**, then this tensor can be null regardless of the value of *ScaleTensor*.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the results to. This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.

### -field AxisCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of axes. This field determines the size of the *Axes* array.

### -field Axes

Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\*** 

The axes along which to calculate the Mean and Variance. 

### -field NormalizeVariance

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

**TRUE** if the Normalization layer includes Variance in the normalization calculation. Otherwise, **FALSE**. If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.

### -field Epsilon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The epsilon value to use to avoid division by zero. A value of 0.00001 is recommended as default.

### -field FusedActivation

Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An optional fused activation layer to apply after the normalization.

## -remarks
**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc). Here, setting the **Axes** array to `{ 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_1`.

## Tensor constraints

*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.

## Tensor support

### DML_FEATURE_LEVEL_3_1 and above

| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Optional input | 1 to 8 | FLOAT32, FLOAT16 |
| BiasTensor | Optional input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_2_1 and above

| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Optional input | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Optional input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also
[Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations)
