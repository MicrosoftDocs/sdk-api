---
UID: NS:directml.DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
title: DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
description: Returns a value representing the sign of each element of *InputTensor*, placing the result into the corresponding element of *OutputTensor*.
tech.root: directml
ms.date: 10/30/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: directml.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - directml.h
api_name:
 - DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
f1_keywords:
 - DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_SIGN_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Returns a value representing the sign of each element of *InputTensor*, placing the result into the corresponding element of *OutputTensor*.

```
f(x) = -1, if x < 0
        1, if x > 0
        0, otherwise // This includes negative zero.
```

This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md)\***

The input tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](./ns-directml-dml_tensor_desc.md)\***

The output tensor to write the results to.

## -remarks

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support

### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16 |

## -see-also
