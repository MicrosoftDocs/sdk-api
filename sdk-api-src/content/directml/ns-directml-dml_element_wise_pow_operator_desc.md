---
UID: NS:directml.DML_ELEMENT_WISE_POW_OPERATOR_DESC
title: DML_ELEMENT_WISE_POW_OPERATOR_DESC
description: Computes each element of *InputTensor* raised to the power of the corresponding element of *ExponentTensor*, placing the result into the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ELEMENT_WISE_POW_OPERATOR_DESC","DML_ELEMENT_WISE_POW_OPERATOR_DESC structure","direct3d12.dml_element_wise_pow_operator_desc","directml/DML_ELEMENT_WISE_POW_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_pow_operator_desc.htm
tech.root: directml
ms.assetid: 72AF58C4-F651-4439-8963-FA64D75A63C3
ms.date: 10/30/2020
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
 - DML_ELEMENT_WISE_POW_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_POW_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_POW_OPERATOR_DESC
---

## -description

Computes each element of *InputTensor* raised to the power of the corresponding element of *ExponentTensor*, placing the result into the corresponding element of *OutputTensor*.

```
f(input, exponent) = pow(input, exponent)
```

Negative bases are supported for exponents with integral values (though datatype can still be float), otherwise this operator returns NaN.

When the input tensor and exponent tensor both have integral data type, this operator guarantees exact results.

This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the input values.

### -field ExponentTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The tensor containing the exponent values.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

### -field ScaleBias

Type: \_Maybenull\_ **const [DML_SCALE_BIAS](/windows/win32/api/directml/ns-directml-dml_scale_bias)\***

An optional scale and bias to apply to the input. If present, this has the effect of applying the function `g(x) = x * scale + bias` to each *input* element prior to computing this operator.

## -remarks
Until `DML_FEATURE_LEVEL_3_0`, *ExponentTensor* _must_ match the type of *InputTensor*.

See [DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_constant_pow_operator_desc) for a POW operator that accepts a `FLOAT` constant for the exponent.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
* *ExponentTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.
* *InputTensor* and *OutputTensor* must have the same *DataType*.

## Tensor support
### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ExponentTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| ExponentTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also

[DML_ELEMENT_WISE_CONSTANT_POW_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_element_wise_constant_pow_operator_desc)
