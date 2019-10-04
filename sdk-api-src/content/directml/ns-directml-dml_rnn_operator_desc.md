---
UID: NS:directml.DML_RNN_OPERATOR_DESC
title: DML_RNN_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML deep learning operator that performs a one-layer simple recurrent neural network (RNN) function on the input, Y = Activation(clip( X * Transpose(W) + Initial_h * Transpose(R) + b)).
old-location: direct3d12\dml_rnn_operator_desc.htm
tech.root: direct3d12
ms.assetid: BF4C0C6F-E02E-4458-AE04-D192AD304512
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_RNN_OPERATOR_DESC, DML_RNN_OPERATOR_DESC structure, direct3d12.dml_rnn_operator_desc, directml/DML_RNN_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_RNN_OPERATOR_DESC"
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
 - DML_RNN_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_RNN_OPERATOR_DESC structure


## -description






Describes a DirectML deep learning operator that performs a one-layer simple recurrent neural network (RNN) function on the input, Y = Activation(clip( X * Transpose(W) + Initial_h * Transpose(R) + b)).


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from, X. Packed (and potentially padded) into one 3-D tensor with the shape of [seq_length, batch_size, input_size].


### -field WeightTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor for the gates, W. Concatenation of Wi and WBi (if bidirectional). The tensor has shape [num_directions, hidden_size, input_size].


### -field RecurrenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the recurrence weight tensor, R. Concatenation of Ri and RBi (if bidirectional). This tensor has shape [num_directions, hidden_size, hidden_size].


### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias tensor for the input gate, B. Concatenation of [Wbi, Rbi], and [WBbi, RBbi] (if bidirectional). This tensor has shape [num_directions, 2 * hidden_size]. If not specified, then defaults to 0.


### -field HiddenInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the hidden node initializer tensor, H. If not specified, then defaults to 0. This tensor has shape [num_directions, batch_size, hidden_size].


### -field SequenceLengthsTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the lengths of the sequences in a batch. If not specified, then all sequences in the batch have length seq_length. This tensor has shape [batch_size].


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

The direction of the operator—forward, reverse, or bidirectional. You can use a default value of <b>DML_RECURRENT_NETWORK_DIRECTION_FORWARD</b>.

