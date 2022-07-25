---
UID: NS:directml.DML_ELEMENT_WISE_QUANTIZED_LINEAR_ADD_OPERATOR_DESC
title: DML_ELEMENT_WISE_QUANTIZED_LINEAR_ADD_OPERATOR_DESC
description: Adds every element in *ATensor* to its corresponding element in *BTensor*, placing the result into the corresponding element of *OutputTensor*.
tech.root: directml
ms.date: 07/02/2021
req.construct-type: structure
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
 - DML_ELEMENT_WISE_QUANTIZED_LINEAR_ADD_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_QUANTIZED_LINEAR_ADD_OPERATOR_DESC
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - directml.h
api_name:
 - DML_ELEMENT_WISE_QUANTIZED_LINEAR_ADD_OPERATOR_DESC
---

## -description

Adds every element in *ATensor* to its corresponding element in *BTensor*, placing the result into the corresponding element of *OutputTensor*. Values contained in *ATensor* and *BTensor* are dequantized using the following equation, and then added and requantized.

```
AValue = (A - AZeroPoint) * AScale
BValue = (B - BZeroPoint) * BScale

OutputValue = AValue + BValue

// For uint8 output, Min = 0, Max = 255
// For int8 output, Min = -128, Max = 127
OutputTensor = clamp(round(OutputValue / OutputScale) + OutputZeroPoint, Min, Max)
```

## -struct-fields

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the left-hand-side inputs.

### -field AScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the desired scale factor for *ATensor*. The expected number of elements in *AScaleTensor* is 1.

### -field AZeroPointTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the desired zero point for *ATensor*. The expected number of elements in *AZeroPointTensor* is 1. *AZeroPointTensor* is an optional tensor that defaults to 0 if not provided.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the right-hand-side inputs.

### -field BScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the desired scale factor for *BTensor*. The expected number of elements in *BScaleTensor* is 1.

### -field BZeroPointTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the desired zero point for *BTensor*. The expected number of elements in *BZeroPointTensor* is 1. *BZeroPointTensor* is an optional tensor that defaults to 0 if not provided.

### -field OutputScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the desired scale factor for *OutputTensor*. This is an input tensor defining the output quantization scale factor to use while quantizing the output values. The expected number of elements in *OutputScaleTensor* is 1.

### -field OutputZeroPointTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the desired zero point for *OutputTensor*. This is an input tensor defining the output quantization zero point to use while quantizing the output values. The expected number of elements in *OutputZeroPointTensor* is 1. *OutputZeroPointTensor* is an optional tensor that defaults to 0 if not provided.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## -remarks

## Availability
This operator was introduced in **DML_FEATURE_LEVEL_4_0**.

## Tensor constraints
* *AScaleTensor*, *ATensor*, *AZeroPointTensor*, *BScaleTensor*, *BTensor*, *BZeroPointTensor*, *OutputScaleTensor*, *OutputTensor*, and *OutputZeroPointTensor* must have the same *DimensionCount*.
* *BTensor* and *BZeroPointTensor* must have the same *DataType*.
* *OutputTensor* and *OutputZeroPointTensor* must have the same *DataType*.
* *ATensor* and *AZeroPointTensor* must have the same *DataType*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 1 to 8 | INT8, UINT8 |
| AScaleTensor | Input | 1 to 8 | FLOAT32 |
| AZeroPointTensor | Optional input | 1 to 8 | INT8, UINT8 |
| BTensor | Input | 1 to 8 | INT8, UINT8 |
| BScaleTensor | Input | 1 to 8 | FLOAT32 |
| BZeroPointTensor | Optional input | 1 to 8 | INT8, UINT8 |
| OutputScaleTensor | Input | 1 to 8 | FLOAT32 |
| OutputZeroPointTensor | Optional input | 1 to 8 | INT8, UINT8 |
| OutputTensor | Output | 1 to 8 | INT8, UINT8 |

## -see-also

* [DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_dequantize_linear_operator_desc)
