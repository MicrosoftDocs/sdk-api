---
UID: NS:directml.DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
title: DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
description: Describes a DirectML operator that performs a local response normalization (LRN) function on the input, y = x / (bias + (alpha / size) * sum(xi^2 for every xi in the local region))^beta.
helpviewer_keywords: ["DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC","DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC structure","direct3d12.dml_local_response_normalization_operator_desc","directml/DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC"]
old-location: direct3d12\dml_local_response_normalization_operator_desc.htm
tech.root: direct3d12
ms.assetid: 43C494DC-4922-4944-A07F-802B43122575
ms.date: 12/5/2018
ms.keywords: DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC, DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC structure, direct3d12.dml_local_response_normalization_operator_desc, directml/DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
f1_keywords:
- directml/DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
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
- DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_LOCAL_RESPONSE_NORMALIZATION_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs a local response normalization (LRN) function on the input, y = x / (bias + (alpha / size) * sum(xi^2 for every xi in the local region))^beta. The data type and size of the input and output tensors must be the same.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from. This tensor's dimensions for the image case are [N, C, H, W], where N is the batch size, C is the number of channels, and H and W are the height and the width of the data. For the non-image case, the dimensions are in the form of [N, C, D1, D2, ..., Dn], where N is the batch size.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to. This tensor's dimensions match those of <i>InputTensor.</i>


### -field CrossChannel

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the LRN layer is channel-wise (cross-channel). Otherwise, <b>FALSE</b>.


### -field LocalSize

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of channels to sum over.


### -field Alpha

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the scaling parameter. You can use a default value of 0.0001.


### -field Beta

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of the exponent. You can use a default value of 0.75.


### -field Bias

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The value of bias. You can use a default value of 1.0.


## -remarks



The operator normalizes over local input regions. The local region is defined across the channels. For an element X[n, c, d1, ..., dk] in a tensor of shape (N x C x D1 x D2, ..., Dk), its region is {X[n, i, d1, ..., dk] | max(0, c - floor((size - 1) / 2)) &lt;= i &lt;= min(C - 1, c + ceil((size - 1) / 2))}.

square_sum[n, c, d1, ..., dk] = sum(X[n, i, d1, ..., dk] ^ 2), where max(0, c - floor((size - 1) / 2)) &lt;= i &lt;= min(C - 1, c + ceil((size - 1) / 2)).

Y[n, c, d1, ..., dk] = X[n, c, d1, ..., dk] / (bias + alpha / size * square_sum[n, c, d1, ..., dk] ) ^ beta.



