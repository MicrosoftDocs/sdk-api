---
UID: NS:directml.DML_BATCH_NORMALIZATION_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_OPERATOR_DESC
description: The DML_BATCH_NORMALIZATION_OPERATOR_DESC structure (directml.h) performs a batch normalization on the input.
helpviewer_keywords: ["DML_BATCH_NORMALIZATION_OPERATOR_DESC","DML_BATCH_NORMALIZATION_OPERATOR_DESC structure","direct3d12.dml_batch_normalization_operator_desc","directml/DML_BATCH_NORMALIZATION_OPERATOR_DESC"]
old-location: direct3d12\dml_batch_normalization_operator_desc.htm
tech.root: directml
ms.assetid: 6589B3EF-1DB9-4E52-B0D2-31C94A725F07
ms.date: 11/30/2022
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

Any dimension in *MeanTensor*, *VarianceTensor*, *ScaleTensor*, and *BiasTensor* can be set to 1, and be automatically broadcast to match *InputTensor*, but otherwise must equal the corresponding dimension's size from *InputTensor*.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Input data.

### -field MeanTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Mean data.

### -field VarianceTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Variance data.

### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Scale data.

### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the Bias data.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor to write the results to.

### -field Spatial

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

**TRUE** to specify that locations are spatial, otherwise **FALSE**. Setting this to **FALSE** will require the Width and Height dimensions of *MeanTensor* and *VarianceTensor* to not be broadcast. This parameter was deprecated in **DML_FEATURE_LEVEL_4_0**, and has no effect.

### -field Epsilon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The epsilon value to use to avoid division by zero.

### -field FusedActivation

Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An optional fused activation layer to apply after the normalization. For more info, see [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations).

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *BiasTensor*, *InputTensor*, *MeanTensor*, *OutputTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.
* *InputTensor* and *OutputTensor* must have the same *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_3_1 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| MeanTensor | Input | { MeanDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| VarianceTensor | Input | { VarianceDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| ScaleTensor | Input | { ScaleDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| BiasTensor | Input | { BiasDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { InputDimensions[] } | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Dimensions | Supported dimension counts | Supported data types |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Input | { InputDimensions[] } | 4 | FLOAT32, FLOAT16 |
| MeanTensor | Input | { MeanDimensions[] } | 4 | FLOAT32, FLOAT16 |
| VarianceTensor | Input | { VarianceDimensions[] } | 4 | FLOAT32, FLOAT16 |
| ScaleTensor | Input | { ScaleDimensions[] } | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Input | { BiasDimensions[] } | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | { InputDimensions[] } | 4 | FLOAT32, FLOAT16 |

## -see-also

* [Using fused operators for improved performance](/windows/ai/directml/dml-fused-activations)
