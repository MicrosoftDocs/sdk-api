---
UID: NS:directml.DML_SPLIT_OPERATOR_DESC
title: DML_SPLIT_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML data reorganization operator that splits the input tensor into multiple output tensors, along the specified axis.
old-location: direct3d12\dml_split_operator_desc.htm
tech.root: direct3d12
ms.assetid: 42FEF441-2B7E-44D3-9889-75869AED4667
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_SPLIT_OPERATOR_DESC, DML_SPLIT_OPERATOR_DESC structure, direct3d12.dml_split_operator_desc, directml/DML_SPLIT_OPERATOR_DESC
ms.topic: struct
f1_keywords: ["directml/DML_SPLIT_OPERATOR_DESC"]
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
 - DML_SPLIT_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_SPLIT_OPERATOR_DESC structure


## -description






Describes a DirectML data reorganization operator that splits the input tensor into multiple output tensors, along the specified axis.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field OutputCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the <i>OutputTensors</i> array.


### -field OutputTensors

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant array of [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the descriptions of the tensors to write the results to.


### -field Axis

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The axis to split on.

