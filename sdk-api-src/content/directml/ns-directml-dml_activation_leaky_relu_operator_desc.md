---
UID: NS:directml.DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC
title: DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC
description: Performs a leaky rectified linear unit (ReLU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC","DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC structure","direct3d12.dml_activation_leaky_relu_operator_desc","directml/DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC"]
old-location: direct3d12\dml_activation_leaky_relu_operator_desc.htm
tech.root: directml
ms.assetid: 75893E5C-D379-47CE-8291-CA00A98D43EA
ms.date: 12/5/2018
ms.keywords: DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC, DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC structure, direct3d12.dml_activation_leaky_relu_operator_desc, directml/DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC
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
 - DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC
 - directml/DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC
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
 - DML_ACTIVATION_LEAKY_RELU_OPERATOR_DESC
---

## -description

Performs a leaky rectified linear unit (ReLU) activation function on every element in *InputTensor*, placing the result into the corresponding element of *OutputTensor*.

```
f(x) = x,         if x >= 0
       Alpha * x, otherwise
```

This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The input tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

### -field Alpha

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The alpha coefficient. A typical default for this value is 0.01.

## -see-also

[DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)

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
