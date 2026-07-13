---
UID: NS:directml.DML_ELEMENT_WISE_NEGATE_OPERATOR_DESC
tech.root: directml
title: DML_ELEMENT_WISE_NEGATE_OPERATOR_DESC
ms.date: 07/22/2022
targetos: Windows
description: Negates each element of *InputTensor*, storing the result into the corresponding element of *OutputTensor*.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: directml.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - directml.h
api_name:
 - DML_ELEMENT_WISE_NEGATE_OPERATOR_DESC
f1_keywords:
 - DML_ELEMENT_WISE_NEGATE_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_NEGATE_OPERATOR_DESC
dev_langs:
 - c++
helpviewer_keywords:
 - DML_ELEMENT_WISE_NEGATE_OPERATOR_DESC
---

## -description

Negates each element of *InputTensor*, storing the result into the corresponding element of *OutputTensor*.

```
f(x) = -x
```

This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The input tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## -remarks

## Availability
This operator was introduced in **DML_FEATURE_LEVEL_5_0**.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8 |

## -see-also
