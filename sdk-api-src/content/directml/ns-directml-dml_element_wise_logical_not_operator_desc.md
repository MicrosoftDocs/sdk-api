---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC
description: Performs a logical NOT on each element of *InputTensor*, placing the result into the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC","DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC structure","direct3d12.dml_element_wise_logical_not_operator_desc","directml/DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_logical_not_operator_desc.htm
tech.root: directml
ms.assetid: 940CF222-4D6C-40E2-A37C-9BB54EE81685
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
 - DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_LOGICAL_NOT_OPERATOR_DESC
---

## -description

Performs a logical NOT on each element of *InputTensor*, placing the result into the corresponding element of *OutputTensor*.

```
f(x) = !x
```

This operator supports in-place execution, meaning that *OutputTensor* is permitted to alias *InputTensor* during binding.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The input tensor to read from.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

The output tensor to write the results to.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*InputTensor* and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 1 to 8 | UINT32, UINT8 |
| OutputTensor | Output | 1 to 8 | UINT32, UINT8 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | UINT32, UINT8 |
| OutputTensor | Output | 4 | UINT32, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | UINT32 |
| OutputTensor | Output | 4 | UINT32 |
