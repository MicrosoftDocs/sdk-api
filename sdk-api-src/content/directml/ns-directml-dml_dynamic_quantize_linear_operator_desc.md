---
UID: NS:directml.DML_DYNAMIC_QUANTIZE_LINEAR_OPERATOR_DESC
title: DML_DYNAMIC_QUANTIZE_LINEAR_OPERATOR_DESC
description: Calculates the quantization scale and zero point values necessary to quantize the *InputTensor*, then applies that quantization, writing the result to *OutputTensor*.
tech.root: directml
ms.date: 07/02/2021
req.construct-type: structure
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
f1_keywords:
 - DML_DYNAMIC_QUANTIZE_LINEAR_OPERATOR_DESC
 - directml/DML_DYNAMIC_QUANTIZE_LINEAR_OPERATOR_DESC
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - directml.h
api_name:
 - DML_DYNAMIC_QUANTIZE_LINEAR_OPERATOR_DESC
---

## -description

Calculates the quantization scale and zero point values necessary to quantize the *InputTensor*, then applies that quantization, writing the result to *OutputTensor*.

> [!IMPORTANT]
> This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.6 and later. Also see [DirectML version history](/windows/ai/directml/dml-version-history).

This operator uses the following equation to quantize.

```
InputMax = Max(InputTensor)
InputMin = Min(InputTensor)

AValue = (A - AZeroPoint) * AScale
BValue = (B - BZeroPoint) * BScale

// For uint8 output, Min = 0, Max = 255
// For int8 output, Min = -128, Max = 127
OutputScale = (InputMax – InputMin) / (Max – Min)

OutputZeroPoint = Min - InputMin / OutputScale

OutputTensor = clamp(round(InputValue / OutputScale) + OutputZeroPoint, Min, Max)
```

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the inputs.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

### -field OutputScaleTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the output scale factor for *OutputTensor*. The expected number of elements in *OutputScaleTensor* is 1. 

### -field OutputZeroPointTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the output zero point for *OutputTensor*. The expected number of elements in *OutputZeroPointTensor* is 1. 

## -remarks

## Availability
This operator was introduced in **DML_FEATURE_LEVEL_4_0**.

## Tensor constraints
* *InputTensor*, *OutputScaleTensor*, *OutputTensor*, and *OutputZeroPointTensor* must have the same *DimensionCount*.
* *OutputTensor* and *OutputZeroPointTensor* must have the same *DataType*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 1 to 8 | INT8, UINT8 |
| OutputScaleTensor | Output | 1 to 8 | FLOAT32 |
| OutputZeroPointTensor | Output | 1 to 8 | INT8, UINT8 |

## -see-also
* [DML_ELEMENT_WISE_DEQUANTIZE_LINEAR_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_dequantize_linear_operator_desc)
