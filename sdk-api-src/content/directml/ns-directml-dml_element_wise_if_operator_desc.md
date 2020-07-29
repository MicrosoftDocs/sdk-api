---
UID: NS:directml.DML_ELEMENT_WISE_IF_OPERATOR_DESC
title: DML_ELEMENT_WISE_IF_OPERATOR_DESC
description: Describes a DirectML math operator that essentially performs a ternary `if` statement.
tech.root: directml
ms.date: 01/30/2020
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
 - directml/DML_ELEMENT_WISE_IF_OPERATOR_DESC
dev_langs:
 - c++
---

## -description

Describes a DirectML math operator that essentially performs a ternary `if` statement. It evaluates every element in <i>ConditionTensor</i>, and if `true` returns the corresponding element in <i>ATensor</i>, otherwise it returns the corresponding element in <i>BTensor</i>. Each input tensor can broadcast to the output shape.

```
For each condition, a, b in ConditionTensor, ATensor, BTensor
    if (b) then x else y

//  Example.
//  condition = bool [[1, 0], [1, 1]]
//  x = [[1, 2], [3, 4]] // first input
//  y = [[9, 8], [7, 6]] // second input
//  z = [[1, 8], [3, 4]] // output
```

Can be used to functionally build up other aggregate operators, such as LeakyRelu. Here's an illustration in pseudo-code (not the most efficiently, but possible): `LeakyRelu(X) = If(Less(X, 0), Mul(X, alpha), X)`).

## -struct-fields

### -field ConditionTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>Condition</i> tensor to read from.

### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>A</i> tensor to read from.


### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>B</i> tensor to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

## -remarks

## -see-also
