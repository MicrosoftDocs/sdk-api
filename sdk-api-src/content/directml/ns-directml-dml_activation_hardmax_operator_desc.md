---
UID: NS:directml.DML_ACTIVATION_HARDMAX_OPERATOR_DESC
title: DML_ACTIVATION_HARDMAX_OPERATOR_DESC
description: Performs a hardmax function on each element of *InputTensor*, placing the result into the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ACTIVATION_HARDMAX_OPERATOR_DESC","DML_ACTIVATION_HARDMAX_OPERATOR_DESC structure","direct3d12.dml_activation_hardmax_operator_desc","directml/DML_ACTIVATION_HARDMAX_OPERATOR_DESC"]
old-location: direct3d12\dml_activation_hardmax_operator_desc.htm
tech.root: directml
ms.assetid: 1624348B-F871-4645-848F-3E108D3CC7B1
ms.date: 12/5/2018
ms.keywords: DML_ACTIVATION_HARDMAX_OPERATOR_DESC, DML_ACTIVATION_HARDMAX_OPERATOR_DESC structure, direct3d12.dml_activation_hardmax_operator_desc, directml/DML_ACTIVATION_HARDMAX_OPERATOR_DESC
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
 - DML_ACTIVATION_HARDMAX_OPERATOR_DESC
 - directml/DML_ACTIVATION_HARDMAX_OPERATOR_DESC
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
 - DML_ACTIVATION_HARDMAX_OPERATOR_DESC
---

## -description

Performs a hardmax function on each element of *InputTensor*, placing the result into the corresponding element of *OutputTensor*.

The operator computes the hardmax (1 for the first occurrence of the largest value in the layer, and 0 for all other values) of each row in the given input.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor to read from for the input. This tensor must have an *effective rank* no greater than 2. The effective rank of a tensor is the *DimensionCount* of the tensor, excluding leftmost dimensions of size 1. For example a tensor size of `{ 1, 1, BatchCount, Width }` is valid, and is equivalent to a tensor of sizes `{ BatchCount, Width }`.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## -remarks

The operator computes the hardmax (1 for the first maximum value, and 0 for all others) values for each layer in the batch of the given input. The input is a 2-D tensor (Tensor) of size (batch_size x input_feature_dimensions). The output tensor has the same shape and contains the hardmax values of the corresponding input.

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

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 to 5 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 to 5 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also

[DML_ARGMAX_OPERATOR_DESC structure](/windows/win32/api/directml/ns-directml-dml_argmax_operator_desc)
