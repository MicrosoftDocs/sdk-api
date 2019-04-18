---
UID: NS:directml.DML_CAST_OPERATOR_DESC
title: DML_CAST_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML data reorganization operator that performs the cast function f(x) = cast(x), casting each element in the input to the data type of the output tensor, and storing the result in the corresponding element in the output.
old-location: direct3d12\dml_cast_operator_desc.htm
tech.root: direct3d12
ms.assetid: 6314667B-E22A-48E4-9B0D-07C8D948160C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_CAST_OPERATOR_DESC, DML_CAST_OPERATOR_DESC structure, direct3d12.dml_cast_operator_desc, directml/DML_CAST_OPERATOR_DESC
ms.topic: struct
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
 - DML_CAST_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_CAST_OPERATOR_DESC structure


## -description






Describes a DirectML data reorganization operator that performs the cast function f(x) = cast(x), casting each element in the input to  the data type of the output tensor, and storing the result in the corresponding element in the output.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

