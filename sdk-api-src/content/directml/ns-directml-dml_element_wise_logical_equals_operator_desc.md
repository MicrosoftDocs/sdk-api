---
UID: NS:directml.DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC
title: DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC
description: Describes a DirectML math operator that performs a logical equality function between every element in ATensor and its corresponding element in BTensor, f(a, b) = (a == b).
helpviewer_keywords: ["DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC","DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC structure","direct3d12.dml_element_wise_logical_equals_operator_desc","directml/DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC"]
old-location: direct3d12\dml_element_wise_logical_equals_operator_desc.htm
tech.root: direct3d12
ms.assetid: 4CCDDBB9-B89B-4A63-91CB-1B091D17F942
ms.date: 12/5/2018
ms.keywords: DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC, DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC structure, direct3d12.dml_element_wise_logical_equals_operator_desc, directml/DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC
f1_keywords:
- directml/DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_ELEMENT_WISE_LOGICAL_EQUALS_OPERATOR_DESC structure


## -description






Describes a DirectML math operator that performs a logical equality function between every element in <i>ATensor</i> and its corresponding element in <i>BTensor</i>, f(a, b) = (a == b).


## -struct-fields




### -field ATensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>A</i> tensor to read from.


### -field BTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the <i>B</i> tensor to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

