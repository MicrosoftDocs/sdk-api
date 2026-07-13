---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC
description: Performs a logical AND on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.
helpviewer_keywords: ["DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC","DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC structure","direct3d12.dml_element_wise_logical_and_operator_desc","directml/DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_logical_and_operator_desc.htm
tech.root: directml
ms.assetid: B3C7CAD0-08D8-426A-8881-DF826B8DA555
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
 - DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC
 - directml/DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC
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
 - DML_ELEMENT_WISE_LOGICAL_AND_OPERATOR_DESC
---

## -description

Performs a logical AND on each pair of corresponding elements of the input tensors, placing the result (1 for true, 0 for false) into the corresponding element of *OutputTensor*.

```
f(a, b) = (a && b)
```

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
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*ATensor*, *BTensor*, and *OutputTensor* must have the same *DataType*, *DimensionCount*, and *Sizes*.

## Tensor support
### DML_FEATURE_LEVEL_3_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 1 to 8 | UINT32, UINT8 |
| BTensor | Input | 1 to 8 | UINT32, UINT8 |
| OutputTensor | Output | 1 to 8 | UINT32, UINT8 |

### DML_FEATURE_LEVEL_2_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 | UINT32, UINT8 |
| BTensor | Input | 4 | UINT32, UINT8 |
| OutputTensor | Output | 4 | UINT32, UINT8 |

### DML_FEATURE_LEVEL_1_0 and above
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Input | 4 | UINT32 |
| BTensor | Input | 4 | UINT32 |
| OutputTensor | Output | 4 | UINT32 |
