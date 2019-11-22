---
UID: NS:directml.DML_TOP_K_OPERATOR_DESC
title: DML_TOP_K_OPERATOR_DESC

description: Describes a DirectML reduction operator that retrieves the top K elements along a specified axis.
old-location: direct3d12\dml_top_k_operator_desc.htm
tech.root: direct3d12
ms.assetid: BB0FD5F7-BCD8-42E0-A037-4411AFF386C2

ms.date: 12/5/2018
ms.keywords: DML_TOP_K_OPERATOR_DESC, DML_TOP_K_OPERATOR_DESC structure, direct3d12.dml_top_k_operator_desc, directml/DML_TOP_K_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_TOP_K_OPERATOR_DESC"
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
 - DML_TOP_K_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_TOP_K_OPERATOR_DESC structure


## -description






Describes a DirectML reduction operator that retrieves the top K elements along a specified axis.

 Given an input tensor of shape [a_1, a_2, ..., a_n, r] and integer argument k, the operator returns two outputs, as detailed in the descriptions of the output parameters below. Given two equivalent values, the operator uses the indices along the axis as a tiebreaker. That is, the element with the lower index appears first.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field OutputValueTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the resulting values to. This is a tensor of shape [a_1, a_2, ..., a_{axis-1}, k, a_{axis+1}, ... a_n], containing the top K values from the input tensor along the specified axis.


### -field OutputIndexTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the resulting indices  to. This is a tensor of shape [a_1, a_2, ..., a_{axis-1}, k, a_{axis+1}, ... a_n], containing the corresponding input tensor indices for the top K values.


### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The dimension on which to do the sort.


### -field K

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of top elements to retrieve.

