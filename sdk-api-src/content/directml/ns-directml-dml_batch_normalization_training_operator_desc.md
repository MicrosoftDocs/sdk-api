---
UID: NS:directml.DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC
tech.root: directml
title: DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC
ms.date: 11/30/2022
targetos: Windows
description: The DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC structure (directml.h) performs a batch normalization on the input.
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
 - DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC
f1_keywords:
 - DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC
 - directml/DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC
dev_langs:
 - c++
helpviewer_keywords:
 - DML_BATCH_NORMALIZATION_TRAINING_OPERATOR_DESC
---

## -description

Performs a batch normalization on the input. This operator performs the following computation: `Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias + FusedAdd)`.

Any dimension in *ScaleTensor* and *BiasTensor* can be set to 1, and be automatically broadcast to match *InputTensor*, but otherwise must equal the corresponding dimension's size from *InputTensor*. *MeanTensor* and *VarianceTensor* are computed on the input across the set of dimensions for which *ScaleTensor* and *BiasTensor* sizes equal one.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Input data.

### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Scale data. 

### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Bias  data. 

### -field FusedAddTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing data that is added to the result prior to FusedActivation, if any.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the results to.

### -field OutputMeanTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the mean of the input to.

### -field OutputVarianceTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the variance of the input to.

### -field Epsilon

Type: [**FLOAT**](/windows/desktop/winprog/windows-data-types)

The epsilon value to use to avoid division by zero.

### -field FusedActivation

Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An optional fused activation layer to apply after the normalization. For more info, see [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations).

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_4_1`.

## Tensor constraints
* *BiasTensor*, *FusedAddTensor*, *InputTensor*, *OutputMeanTensor*, *OutputTensor*, *OutputVarianceTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.
* *BiasTensor*, *OutputMeanTensor*, *OutputVarianceTensor*, and *ScaleTensor* must have the same *Sizes*.
* *FusedAddTensor*, *InputTensor*, and *OutputTensor* must have the same *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Input | { ScaleDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| BiasTensor | Input | { ScaleDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| FusedAddTensor | Optional input | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| OutputMeanTensor | Output | { ScaleDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| OutputVarianceTensor | Output | { ScaleDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |

## -see-also

* [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations)
