---
UID: NS:directml.DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC
title: DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC
description: Performs the following linear quantization function on every element in *InputTensor* with respect to its corresponding element in *ScaleTensor* and `ZeroPointTensor`, placing the results in the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC","DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC structure","direct3d12.dml_element_wise_quantize_linear_operator_desc","directml/DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_quantize_linear_operator_desc.htm
tech.root: directml
ms.assetid: 46415049-2978-4162-B94C-B600EA91992C
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
 - DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_QUANTIZE_LINEAR_OPERATOR_DESC
---

## -description

Performs the following linear quantization function on every element in *InputTensor* with respect to its corresponding element in *ScaleTensor* and *ZeroPointTensor*, placing the results in the corresponding element of *OutputTensor*.

```
// For uint8 output, Min = 0, Max = 255
// For int8 output, Min = -128, Max = 127
f(input, scale, zero_point) = clamp(round(input / scale) + zero_point, Min, Max)
```

Quantizing involves converting to a lower-precision data type in order to accelerate arithmetic. It's a common way to increase performance at the cost of precision. A group of 8-bit values can be computed faster than a group of 32-bit values can.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the inputs.

### -field ScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the scales.

> [!NOTE]
> A scale value of 0 results in undefined behavior.

If *InputTensor* is **INT32**, then *ScaleTensor* must be **FLOAT32**. Otherwise, *ScaleTensor* must have the same *DataType* as *InputTensor*.

### -field ZeroPointTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the desired zero point for the quantization.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *InputTensor*, *OutputTensor*, *ScaleTensor*, and *ZeroPointTensor* must have the same *DimensionCount* and *Sizes*.
* *OutputTensor* and *ZeroPointTensor* must have the same *DataType*.

## Tensor support
### DML_FEATURE_LEVEL_6_2 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32 |
| ScaleTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| ZeroPointTensor | Optional input | 1 to 8 | INT8, UINT8 |
| OutputTensor | Output | 1 to 8 | INT8, UINT8 |

### DML_FEATURE_LEVEL_6_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32 |
| ScaleTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| ZeroPointTensor | Input | 1 to 8 | INT8, UINT8 |
| OutputTensor | Output | 1 to 8 | INT8, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, INT32 |
| ScaleTensor | Input | 1 to 8 | FLOAT32 |
| ZeroPointTensor | Input | 1 to 8 | INT8, UINT8 |
| OutputTensor | Output | 1 to 8 | INT8, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, INT32 |
| ScaleTensor | Input | 4 | FLOAT32 |
| ZeroPointTensor | Input | 4 | INT8, UINT8 |
| OutputTensor | Output | 4 | INT8, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32 |
| ScaleTensor | Input | 4 | FLOAT32 |
| ZeroPointTensor | Input | 4 | UINT8 |
| OutputTensor | Output | 4 | UINT8 |

## -see-also

[DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_dequantize_linear_operator_desc)
