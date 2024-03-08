---
UID: NS:directml.DML_BATCH_NORMALIZATION_TRAINING_GRAD_OPERATOR_DESC
tech.root: directml
title: DML_BATCH_NORMALIZATION_TRAINING_GRAD_OPERATOR_DESC
ms.date: 07/22/2022
targetos: Windows
description: Computes backpropagation gradients for [batch normalization training](/windows/win32/api/directml/ns-directml-dml_batch_normalization_training_operator_desc).
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
 - DML_BATCH_NORMALIZATION_TRAINING_GRAD_OPERATOR_DESC
f1_keywords:
 - DML_BATCH_NORMALIZATION_TRAINING_GRAD_OPERATOR_DESC
 - directml/DML_BATCH_NORMALIZATION_TRAINING_GRAD_OPERATOR_DESC
dev_langs:
 - c++
helpviewer_keywords:
 - DML_BATCH_NORMALIZATION_TRAINING_GRAD_OPERATOR_DESC
---

## -description

Computes backpropagation gradients for [batch normalization training](/windows/win32/api/directml/ns-directml-dml_batch_normalization_training_operator_desc).

This operator performs multiple computations, which are detailed in the separate output descriptions.

Any dimension in *MeanTensor*, *VarianceTensor*, and *ScaleTensor* can be set to 1, and be automatically broadcast to match *InputTensor*, but otherwise must equal the corresponding dimension's size from *InputTensor*. 

*OutputScaleGradientTensor* and *OutputBiasGradientTensor* are computed using sums across the set of dimensions for which *MeanTensor*, *ScaleTensor* and *VarianceTensor* sizes equal one.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the input data. This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_training_operator_desc) in the forward pass.

### -field InputGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The incoming gradient tensor. This is typically obtained from the output of backpropagation of a preceding layer.  

### -field MeanTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the mean data. This is typically the same tensor that was returned by *MeanTensor* from [**DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_training_operator_desc) in the forward pass.

### -field VarianceTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the variance data. This is typically the same tensor that was returned as the *OutputVarianceTensor* from [**DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_training_operator_desc) in the forward pass. 

### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the scale data.

### -field OutputGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

For every corresponding value in the inputs:  

```
Coef0 = 1.0f / sqrt(Variance + Epsilon)
Coef1 = InputGradient * (Input - mean(Input))
InputGradientCentered = InputGradient - mean(InputGradient)
InputCentered = InputCentered - mean(InputCentered)
OutputGradient = Scale * Coef0 * (InputGradientCentered - InputCentered * mean(Coef1) / (Variance + Epsilon))
```

### -field OutputScaleGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The following computation is done or every corresponding value in the inputs: `OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

### -field OutputBiasGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The following computation is done or every corresponding value in the inputs: `OutputBiasGradient = sum(InputGradient)`  

### -field Epsilon

Type: [**FLOAT**](/windows/desktop/winprog/windows-data-types)

A small float value added to the variance to avoid zero.

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_4_1`.

## Tensor constraints
* *InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.
* *MeanTensor*, *OutputBiasGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *Sizes*.
* *InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| MeanTensor | Input | { MeanDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| VarianceTensor | Input | { MeanDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Input | { MeanDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| OutputScaleGradientTensor | Output | { MeanDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| OutputBiasGradientTensor | Output | { MeanDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |

## -see-also
