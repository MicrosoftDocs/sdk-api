---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC","DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure","direct3d12.dml_element_wise_bit_shift_right_operator_desc","directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC"]
tech.root: directml
ms.date: 10/29/2020
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
 - DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
---

## -description

Performs a logical right shift of each element of *ATensor* by a number of bits given by the corresponding element of *BTensor*, placing the result into the corresponding element of *OutputTensor*.

```
f(a, b) = (a >> b)
```

The bitwise operation is applied to tensor data in its native encoding. Therefore, the tensor data type is ignored except for determining the width of each element.

This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias one of the input tensors during binding.

## -struct-fields

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the left-hand side inputs.

### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the right-hand side inputs.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_2_1`.

## Tensor constraints
*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support

### DML_FEATURE_LEVEL_4_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 1 to 8 | UINT64, UINT32, UINT16, UINT8 |
| BTensor | Input | 1 to 8 | UINT64, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | UINT64, UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 1 to 8 | UINT32, UINT16, UINT8 |
| BTensor | Input | 1 to 8 | UINT32, UINT16, UINT8 |
| OutputTensor | Output | 1 to 8 | UINT32, UINT16, UINT8 |

### DML_FEATURE_LEVEL_2_1 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 | UINT32, UINT16, UINT8 |
| BTensor | Input | 4 | UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | UINT32, UINT16, UINT8 |
