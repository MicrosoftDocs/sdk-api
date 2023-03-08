---
UID: NS:directml.DML_ELEMENT_WISE_RECIP_OPERATOR_DESC
title: DML_ELEMENT_WISE_RECIP_OPERATOR_DESC
description: Computes the reciprocal for each element of the input tensor, placing the result into the corresponding element of the output tensor.
helpviewer_keywords: ["DML_ELEMENT_WISE_RECIP_OPERATOR_DESC","DML_ELEMENT_WISE_RECIP_OPERATOR_DESC structure","direct3d12.dml_element_wise_recip_operator_desc","directml/DML_ELEMENT_WISE_RECIP_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_recip_operator_desc.htm
tech.root: directml
ms.assetid: B5198895-7F09-4163-8F9E-F23FE0D92724
ms.date: 10/30/2020
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
 - DML_ELEMENT_WISE_RECIP_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_RECIP_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_RECIP_OPERATOR_DESC
---

## -description

Computes the reciprocal for each element of the input tensor, placing the result into the corresponding element of the output tensor.

```
f(x) = 1 / x
```

This operator supports in-place execution, meaning that the output tensor is permitted to alias the input tensor during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to read from for the first input tensor, x.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

### -field ScaleBias

Type: \_Maybenull\_ **const [DML_SCALE_BIAS](/windows/win32/api/directml/ns-directml-dml_scale_bias)\***

An optional scale and bias to apply to the input. If present, this has the effect of applying the function `g(x) = x * scale + bias` to each *input* element prior to computing this operator.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |
