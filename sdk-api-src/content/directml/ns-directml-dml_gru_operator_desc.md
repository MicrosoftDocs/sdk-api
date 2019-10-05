---
UID: NS:directml.DML_GRU_OPERATOR_DESC
title: DML_GRU_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML deep learning operator that performs a (standard layers) one-layer gated recurrent unit (GRU) function on the input.
old-location: direct3d12\dml_gru_operator_desc.htm
tech.root: direct3d12
ms.assetid: 233D9FBC-087D-42B4-84E2-2FDBD6DFF033
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_GRU_OPERATOR_DESC, DML_GRU_OPERATOR_DESC structure, direct3d12.dml_gru_operator_desc, directml/DML_GRU_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_GRU_OPERATOR_DESC"
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
 - DML_GRU_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_GRU_OPERATOR_DESC structure


## -description






Describes a DirectML deep learning operator that performs a (standard layers) one-layer gated recurrent unit (GRU) function on the input.

Z = Activation1(clip( X * transpose(W1) + Initial_h1 * transpose(R1) + b1))

R = Activation1(clip( X * transpose(W2) + Initial_h1 * transpose(R2) + b2))

C = Initial_h1 .* R

O = Activation2(clip( X * transpose(W3) + Initial_h1 * transpose(R3) + b3))

Y = (1-Z) .* O + Z .* Initial_h1

(W = [W1, W2, W3]; b1 = B[0, :] + B[3*hidden_size]; b2 = B[1, :] + B[4*hidden_size, :]; b3 = B[2, :] + B[4*hidden_size, :];)


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from for the input tensor, X.


### -field WeightTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor, W.


### -field RecurrenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the recurrence tensor, R.


### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias tensor, B.


### -field HiddenInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the hidden node initializer tensor, H.


### -field SequenceLengthsTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the sequence lengths.


### -field OutputSequenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the concatenation of all the intermediate output values of the hidden nodes.  This tensor has shape [seq_length, num_directions, batch_size, hidden_size].


### -field OutputSingleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the last output value of the hidden nodes.  This tensor has shape [num_directions, batch_size, hidden_size].


### -field ActivationDescCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the <i>ActivationDescs</i> array.


### -field ActivationDescs

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

A pointer to a constant array of [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the descriptions of the activation operators.


### -field Direction

Type: **const [DML_RECURRENT_NETWORK_DIRECTION](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction)\***

The direction of the operator—forward, reverse, or bidirectional.


### -field LinearBeforeReset

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to specify that, when computing the output of the hidden gate, the linear transformation should be applied before multiplying by the output of the reset gate. Otherwise, <b>FALSE</b>.

