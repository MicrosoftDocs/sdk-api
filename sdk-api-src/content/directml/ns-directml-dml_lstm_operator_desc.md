---
UID: NS:directml.DML_LSTM_OPERATOR_DESC
title: DML_LSTM_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML deep learning operator that performs a one-layer long short term memory (LSTM) function on the input.
old-location: direct3d12\dml_lstm_operator_desc.htm
tech.root: direct3d12
ms.assetid: B2225A27-EB5B-46BC-A224-6A07D869C001
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_LSTM_OPERATOR_DESC, DML_LSTM_OPERATOR_DESC structure, direct3d12.dml_lstm_operator_desc, directml/DML_LSTM_OPERATOR_DESC
ms.topic: struct
f1_keywords: ["directml/DML_LSTM_OPERATOR_DESC"]
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
 - DML_LSTM_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_LSTM_OPERATOR_DESC structure


## -description






Describes a DirectML deep learning operator that performs a one-layer long short term memory (LSTM) function on the input.

I = Activation1(clip(X * transpose(W1) + Initial_h1 * transpose(R1) + p .* initial_c + b1))

F = Activation1(clip(X * transpose(W2) + Initial_h1 * transpose(R2) +  p .* initial_c + b2))

Z = Activation2(clip(X * transpose(W3) + Initial_h1 * transpose(R3) + b3))

C = Initial_h1 .* F + I .* Z

O = Activation2(clip( X * tr(W4) + Initial_h1 * tr(R4) + p .* initial_c + b4))

Y = Activation3(C) .* O

(W = [W1, W2, W3, W4]; b1 = B[0, :] + B[4*hidden_size]; b2 = B[1, :] + B[5*hidden_size, :]; b3 = B[2, :] + B[6*hidden_size, :]; b4 = B[3, :] + B[7*hidden_size, :];)


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from, X. Packed (and potentially padded) into one 3-D tensor with the shape of [seq_length, batch_size, input_size].


### -field WeightTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor for the gates, W. Concatenation of W[iofc] and WB[iofc] (if bidirectional) along dimension 0. The tensor has shape [num_directions, 4 * hidden_size, input_size].


### -field RecurrenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the recurrence weight tensor, R. Concatenation of R[iofc] and RB[iofc] (if bidirectional) along dimension 0. This tensor has shape [num_directions, 4 * hidden_size, hidden_size].


### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias tensor for the input gate, B. Concatenation of [Wb[iofc], Rb[iofc]], and [WBb[iofc], RBb[iofc]] (if bidirectional) along dimension 0. This tensor has shape [num_directions, 8 * hidden_size]. If not specified, then defaults to 0.


### -field HiddenInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the hidden node initializer tensor, H. If not specified, then defaults to 0. This tensor has shape [num_directions, batch_size, hidden_size].


### -field CellMemInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the cell initializer tensor. If not specified, then defaults to 0. This tensor has shape [num_directions, batch_size, hidden_size].


### -field SequenceLengthsTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the lengths of the sequences in a batch. If not specified, then all sequences in the batch have length seq_length. This tensor has shape [batch_size].


### -field PeepholeTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor for peepholes. If not specified, then defaults to 0. Concatenation of P[iof] and PB[iof] (if bidirectional) along dimension 0. This tensor has shape [num_directions, 3 * hidden_size].


### -field OutputSequenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the concatenation of all the intermediate output values of the hidden nodes.  This tensor has shape [seq_length, num_directions, batch_size, hidden_size].


### -field OutputSingleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the last output value of the hidden nodes.  This tensor has shape [num_directions, batch_size, hidden_size].


### -field OutputCellSingleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the last output value of the cell.  This tensor has shape [num_directions, batch_size, hidden_size].


### -field ActivationDescCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the <i>ActivationDescs</i> array.


### -field ActivationDescs

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

A pointer to a constant array of [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the descriptions of the activation operators.


### -field Direction

Type: **const [DML_RECURRENT_NETWORK_DIRECTION](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction)\***

The direction of the operator—forward, reverse, or bidirectional. You can use a default value of <b>DML_RECURRENT_NETWORK_DIRECTION_FORWARD</b>.


### -field ClipThreshold

Type: <b>float</b>

The cell clip threshold. Clipping bounds the elements of a tensor in the range of [-threshold, +threshold], and is applied to the input of activations.


### -field UseClipThreshold

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if <i>ClipThreshold</i> should be used. Otherwise, <b>FALSE</b>.


### -field CoupleInputForget

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the input and forget gates should be coupled. Otherwise, <b>FALSE</b>.

