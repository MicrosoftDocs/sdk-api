---
UID: NS:directml.DML_ELEMENT_WISE_IF_OPERATOR_DESC
title: DML_ELEMENT_WISE_IF_OPERATOR_DESC
description: Selects elements either from *ATensor* or *BTensor*, depending on the value of the corresponding element in *ConditionTensor*. Non-zero elements of *ConditionTensor* select from *ATensor*, while zero-valued elements select from *BTensor*.
tech.root: directml
ms.date: 01/19/2022
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
 - DML_ELEMENT_WISE_IF_OPERATOR_DESC
f1_keywords:
 - DML_ELEMENT_WISE_IF_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_IF_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Selects elements either from *ATensor* or *BTensor*, depending on the value of the corresponding element in *ConditionTensor*. Non-zero elements of *ConditionTensor* select from *ATensor*, while zero-valued elements select from *BTensor*.

```
f(cond, a, b) = a, if cond != 0
                b, otherwise

Example:
    [[1, 0], [1, 1]] // ConditionTensor
    [[1, 2], [3, 4]] // ATensor
    [[9, 8], [7, 6]] // BTensor

    [[1, 8], [3, 4]] // Output
```

## -struct-fields

### -field ConditionTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The condition tensor to read from.

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the left-hand side inputs.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the right-hand side inputs.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## -remarks
Can be used to functionally build up other aggregate operators, such as LeakyRelu. Here's an illustration in pseudo-code (not the most efficient way, but possible): `LeakyRelu(x) = If(Less(x, 0), Mul(x, alpha), x)`.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_0`.

## Tensor constraints
* *ATensor*, *BTensor*, *ConditionTensor*, and *OutputTensor* must have the same *DimensionCount* and *Sizes*.
* *ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*.

## Tensor support
### DML_FEATURE_LEVEL_5_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ConditionTensor | Input | 1 to 8 | UINT8 |
| ATensor | Input | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| BTensor | Input | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT64, FLOAT32, FLOAT16, INT64, INT32, INT16, INT8, UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ConditionTensor | Input | 1 to 8 | UINT8 |
| ATensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| BTensor | Input | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ConditionTensor | Input | 4 | UINT8 |
| ATensor | Input | 4 | FLOAT16 |
| BTensor | Input | 4 | FLOAT16 |
| OutputTensor | Output | 4 | FLOAT16 |

## -see-also
