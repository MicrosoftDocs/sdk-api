---
UID: NS:directml.DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
title: DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
description: Computes backpropagation gradients for a rectified linear unit (ReLU).
helpviewer_keywords: ["DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC","DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC structure","direct3d12.dml_activation_relu_grad_operator_desc","directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC"]
tech.root: directml
ms.date: 07/20/2022
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
 - DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
 - directml/DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
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
 - DML_ACTIVATION_RELU_GRAD_OPERATOR_DESC
---

## -description

Computes backpropagation gradients for a rectified linear unit (ReLU). This operator performs the following element-wise computation.

```
X = InputTensor
dY = InputGradientTensor

OutputGradientTensor = (X > 0 ? dY : 0)
```

The corresponding forward-pass operator is [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc).

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The input (feature) tensor. This is typically the same input as was provided during the forward pass (see [DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)).

### -field InputGradientTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The incoming gradient tensor. This is typically obtained from the output of backpropagation of a preceding layer. The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An output tensor containing the backpropagated gradients. The *Sizes* and *DataType* of this tensor must exactly match those of the *InputTensor*.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_3_0`.

## Tensor constraints
*InputGradientTensor*, *InputTensor*, and *OutputGradientTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_5_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8 |
| InputGradientTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8 |
| OutputGradientTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8 |

### DML_FEATURE_LEVEL_4_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| InputGradientTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputGradientTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

## -see-also
[DML_ACTIVATION_RELU_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_activation_relu_operator_desc)
