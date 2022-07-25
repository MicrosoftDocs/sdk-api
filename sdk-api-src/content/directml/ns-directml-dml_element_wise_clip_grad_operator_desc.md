---
UID: NS:directml.DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
title: DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
description: Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).
helpviewer_keywords: ["DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC","DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC structure","direct3d12.dml_element_wise_clip_grad_operator_desc","directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC"]
ms.topic: reference
tech.root: directml
ms.date: 01/19/2022
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
 - DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_CLIP_GRAD_OPERATOR_DESC
---

## -description

Computes backpropagation gradients for [element-wise clip](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc).

```
f(x, gradient) = if x <= Min then 0
                 if x >= Max then 0
                 else        then gradient
```

This operator supports in-place execution, meaning `OutputTensor` is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The input feature tensor. This is typically the same tensor that was provided as the *InputTensor* to [DML_ELEMENT_WISE_CLIP_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_clip_operator_desc) in the forward pass.

### -field InputGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The incoming gradient tensor. This is typically obtained from the output of backpropagation of a preceding layer. Typically this tensor would have the same sizes as the *output* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.

### -field OutputGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An output tensor containing the backpropagated gradients. Typically this tensor would have the same sizes as the *input* of the corresponding **DML_OPERATOR_ELEMENT_WISE_CLIP** in the forward pass.

### -field Min

Type: **[FLOAT](../../winprog/windows-data-types.md)**

The minimum value. If x is at or below this value, then the gradient result is 0.

### -field Max

Type: **[FLOAT](../../winprog/windows-data-types.md)**

The maximum value. If x is at or above this value, then the gradient result is 0.

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_3_1`.

## Tensor constraints
*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| InputGradientTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| InputGradientTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputGradientTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## -see-also
