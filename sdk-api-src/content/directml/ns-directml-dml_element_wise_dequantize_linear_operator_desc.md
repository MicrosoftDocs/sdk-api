---
UID: NS:directml.DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
title: DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
description: Performs the following linear dequantization function on every element in *InputTensor* with respect to its corresponding element in *ScaleTensor* and `ZeroPointTensor`, placing the results in the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC","DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC structure","direct3d12.dml_element_wise_dequantize_linear_operator_desc","directml/DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_dequantize_linear_operator_desc.htm
tech.root: directml
ms.assetid: 474CB378-3EFC-414F-B75F-D41577D0787D
ms.date: 08/21/2024
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
 - DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC
---

## -description

Performs the following linear dequantization function on every element in *InputTensor* with respect to its corresponding element in *ScaleTensor* and `ZeroPointTensor`, placing the results in the corresponding element of *OutputTensor*.

```
f(input, scale, zero_point) = (input - zero_point) * scale
```

Quantization is a common way to increase performance at the cost of precision. A group of 8-bit int values can be computed faster than a group of 32-bit float values can. Dequantizing converts the encoded data back to its domain.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the inputs.

### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the scales.
A scale value of 0 will result in undefined behavior.

> [!NOTE]
> A scale value of 0 results in undefined behavior.

### -field ZeroPointTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the zero point that was used for quantization.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *InputTensor*, *OutputTensor*, *ScaleTensor*, and *ZeroPointTensor* must have the same *DimensionCount* and *Sizes*.
* *InputTensor* and *ZeroPointTensor* must have the same *DataType*.
* *OutputTensor* and *ScaleTensor* must have the same *DataType*.

## Tensor support
### DML_FEATURE_LEVEL_6_2 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ScaleTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| ZeroPointTensor | Optional input | 1 to 8 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_6_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ScaleTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| ZeroPointTensor | Input | 1 to 8 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ScaleTensor | Input | 1 to 8 | FLOAT32 |
| ZeroPointTensor | Input | 1 to 8 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ScaleTensor | Input | 4 | FLOAT32 |
| ZeroPointTensor | Input | 4 | INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | FLOAT32 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | UINT8 |
| ScaleTensor | Input | 4 | FLOAT32 |
| ZeroPointTensor | Input | 4 | UINT8 |
| OutputTensor | Output | 4 | FLOAT32 |

## -see-also

[DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_quantize_linear_operator_desc)
