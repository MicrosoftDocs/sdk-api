---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
description: Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).
helpviewer_keywords: ["DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC","DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC structure","direct3d12.dml_local_response_normalization_grad_operator_desc","directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC"]
ms.topic: reference
tech.root: directml
ms.date: 07/06/2021
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
 - DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
 - directml/DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
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
 - DML_LOCAL_RESPONSE_NORMALIZATION_GRAD_OPERATOR_DESC
---

## -description

Computes backpropagation gradients for [local response normalization](/windows/win32/api/directml/ns-directml-dml_local_response_normalization_operator_desc).

The data type and size of all tensors must be the same.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the input data. This tensor's *Sizes* should be `{ BatchCount, ChannelCount, Height, Width }`.

### -field InputGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The incoming gradient tensor. This is typically obtained from the output of backpropagation of a preceding layer.

### -field OutputGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An output tensor containing the backpropagated gradients.

### -field CrossChannel

Type: **[BOOL](../../winprog/windows-data-types.md)**

**TRUE** if the LRN layer sums across channels; **FALSE** if the LRN layer sums across spatial dimensions.

### -field LocalSize

Type: **[UINT](../../winprog/windows-data-types.md)**

The maximum number of elements to sum over per dimension (the local region is clipped so that all elements are within bounds). If *CrossChannel* is **TRUE**, then this is the width and height of the local region. If *CrossChannel* is **FALSE**, then this is the number of elements in the local region. This value must be at least 1.

### -field Alpha

Type: **[FLOAT](../../winprog/windows-data-types.md)**

The value of the scaling parameter. We recommend a value of 0.0001 as default.

### -field Beta

Type: **[FLOAT](../../winprog/windows-data-types.md)**

The value of the exponent. We recommend a value of 0.75 as default.

### -field Bias

Type: **[FLOAT](../../winprog/windows-data-types.md)**

The value of bias. We recommend a value of 1 as default.

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_3_1`.

## Tensor constraints
*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType* and *Sizes*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also
