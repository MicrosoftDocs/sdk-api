---
UID: NS:directml.DML_ACTIVATION_IDENTITY_OPERATOR_DESC
title: DML_ACTIVATION_IDENTITY_OPERATOR_DESC
description: Performs the identity activation, effectively copying every element of *InputTensor* to the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ACTIVATION_IDENTITY_OPERATOR_DESC","DML_ACTIVATION_IDENTITY_OPERATOR_DESC structure","direct3d12.dml_activation_identity_operator_desc","directml/DML_ACTIVATION_IDENTITY_OPERATOR_DESC"]
old-location: direct3d12\dml_activation_identity_operator_desc.htm
tech.root: directml
ms.assetid: 2D16A1B8-1404-4426-863A-956EC825882F
ms.date: 12/5/2018
ms.keywords: DML_ACTIVATION_IDENTITY_OPERATOR_DESC, DML_ACTIVATION_IDENTITY_OPERATOR_DESC structure, direct3d12.dml_activation_identity_operator_desc, directml/DML_ACTIVATION_IDENTITY_OPERATOR_DESC
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
 - DML_ACTIVATION_IDENTITY_OPERATOR_DESC
 - directml/DML_ACTIVATION_IDENTITY_OPERATOR_DESC
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
 - DML_ACTIVATION_IDENTITY_OPERATOR_DESC
---

## -description

Performs the identity activation, effectively copying every element of *InputTensor* to the corresponding element of *OutputTensor*.

```
f(x) = x
```

This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

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
