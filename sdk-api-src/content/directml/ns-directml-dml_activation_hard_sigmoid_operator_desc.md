---
UID: NS:directml.DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC
title: DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML activation operator that performs a hard sigmoid function on every element in the input, f(x) = max(0, min(alpha * x + beta, 1)).
old-location: direct3d12\dml_activation_hard_sigmoid_operator_desc.htm
tech.root: direct3d12
ms.assetid: 9E6360B5-5B8E-431B-A668-78F69A1E2A43
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC, DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC structure, direct3d12.dml_activation_hard_sigmoid_operator_desc, directml/DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC"
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
 - DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_ACTIVATION_HARD_SIGMOID_OPERATOR_DESC structure


## -description






Describes a DirectML activation operator that performs a hard sigmoid function on every element in the input, f(x) = max(0, min(alpha * x + beta, 1)).

This operator supports in-place execution, meaning the output tensor is permitted to alias the input tensor during binding.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


### -field Alpha

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of alpha.


### -field Beta

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of beta.

