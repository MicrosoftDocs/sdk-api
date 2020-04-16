---
UID: NS:directml.DML_JOIN_OPERATOR_DESC
title: DML_JOIN_OPERATOR_DESC
description: Describes a DirectML operator that performs a join function on an array of input tensors.helpviewer_keywords: ["DML_JOIN_OPERATOR_DESC","DML_JOIN_OPERATOR_DESC structure","direct3d12.dml_join_operator_desc","directml/DML_JOIN_OPERATOR_DESC"]
old-location: direct3d12\dml_join_operator_desc.htm
tech.root: direct3d12
ms.assetid: 48157907-1B0F-4641-949E-0E6C875FF74E
ms.date: 12/5/2018
ms.keywords: DML_JOIN_OPERATOR_DESC, DML_JOIN_OPERATOR_DESC structure, direct3d12.dml_join_operator_desc, directml/DML_JOIN_OPERATOR_DESC
f1_keywords:
- directml/DML_JOIN_OPERATOR_DESC
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
- DML_JOIN_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_JOIN_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs a join function on an array of input tensors.


## -struct-fields




### -field InputCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the <i>InputTensors</i> array.


### -field InputTensors

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant array of [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the descriptions of the tensors to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The axis dimension of the input tensor to join on.

