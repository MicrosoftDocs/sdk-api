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





Describes a DirectML deep learning operator that performs a one-layer simple recurrent neural network (RNN) function on the input. This function is often referred to as the "Input Gate". This operator performs this function multiple times in a loop dictated by sequence length dimension and SequenceLengthsTensor.

**Forward Direction Equation**
for (t = 0; t < seq_length; t++)
{
&nbsp;&nbsp;&nbsp;&nbsp;$H_t = f(X_t*W_i^T + H_{t-1} * R_i^T + W_{bi} + R_{bi})$
}

**Backward Direction Equation**
for (t = seq_length - 1; t >= 0; t--)
{
&nbsp;&nbsp;&nbsp;&nbsp;$H_t = f(X_t*W_{Bi}^T + H_{t-1} * R_{Bi}^T + W_{Bbi} + R_{Bbi})$
}


**Equation Legend**
- $t$ current RNN layer index
- $t-1$ previous RNN layer index. If backwards direction then it means $t+1$ index but still the previously calculated $t$.
- $T$ signifies that a matrix will be transposed before use.
- $*$ signifies a matrix multiplication.
- $+$ signifies a element-wise addition of two matrices.
- $H_t$ output of current RNN index $t$.
- $f()$ activation function dictated by **ActivationDescs**.
- $X_t$ Sub-matrix of the **InputTensor** which is defined by matrix index [$t$, batch_size, input_size].
- $W_i^T$ Forward sub-matrix defined in **WeightTensor** which is defined to be size [1, batch_size, input_size]. This matrix will be transposed before use.
- $W_{Bi}^T$ Backwards sub-matrix defined in **WeightTensor** which is defined to be size [1, batch_size, input_size]. This matrix will be transposed before use.
- $H_{t-1}$ an intermediate tensor which is defined to be the output of the previous layer. For $t = 0$, H_{t-1} is replaced with **HiddenInitTensor**. This is defined to be size [1, batch_size, hidden_size]. A different **HiddenInitTensor** sub-matrix is used for each direction.
- $R_i^T$ Forward sub-matrix of **RecurrenceTensor** which is defined to be size [1, hidden_size, hidden_size]. This matrix will be transposed before use.
- $R_{Bi}^T$ Backwards sub-matrix of **RecurrenceTensor** which is defined to be size [1, hidden_size, hidden_size]. This matrix will be transposed before use.
- $W_{bi}$, $R_{bi}$ are the bias tensors of the weight tensor and recurrence tensor which are one of the sub-matrices of **BiasTensor**. This matrix is size [1,hidden_size] and is broadcasted up to the required size which is [1, batch_size, hidden_size].
- $W_{Bbi}$, $R_{Bbi}$ are the bias tensors for the backwards direction
- $i$ stands for input gate.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from, $X$. Packed (and potentially padded) into one 4-D tensor with the shape of [1, seq_length, batch_size, input_size]. seq_length is the dimension which is mapped to the RNN index, $t$.


### -field WeightTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor for the gates, $W$. Concatenation of $W_i$ and $W_{Bi}$ (if bidirectional). The tensor has shape [1, num_directions, hidden_size, input_size].


### -field RecurrenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the recurrence weight tensor, $R$. Concatenation of $R_i$ and $R_{Bi}$ (if bidirectional). This tensor has shape [1, num_directions, hidden_size, hidden_size].


### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias tensor for the input gate, $B$. Concatenation of [$W_{bi}$, $R_{bi}$], and [$W_{Bbi}$, $R_{Bbi}$] (if bidirectional). This tensor has shape [1, 1, num_directions, 2 * hidden_size]. If not specified, then defaults to 0.


### -field HiddenInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the hidden node initializer tensor, $H_{t-1}$ for the first loop index $t$. If not specified, then defaults to 0. This tensor has shape [1, num_directions, batch_size, hidden_size].


### -field SequenceLengthsTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing an independent seq_length for each element in the batch. If not specified, then all sequences in the batch have length seq_length. This tensor has shape [1, 1, 1, batch_size].


### -field OutputSequenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the concatenation of all the intermediate layer output values of the hidden nodes, $H_t$.  This tensor has shape [seq_length, num_directions, batch_size, hidden_size]. seq_length is mapped to the loop index $t$.


### -field OutputSingleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the final output value of the hidden nodes, $H_t$.  This tensor has shape [1, num_directions, batch_size, hidden_size].


### -field ActivationDescCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the <i>ActivationDescs</i> array.


### -field ActivationDescs

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

A pointer to a constant array of [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the descriptions of the activation operators, $f()$. The number of activation functions is equal to the number of directions. For forwards and backwards directions there are expected to be 1 activation fuction. For Bidirectional there is expected to be 2.


### -field Direction

Type: **const [DML_RECURRENT_NETWORK_DIRECTION](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction)\***

The direction of the operator—forward, backwards, or bidirectional. You can use a default value of <b>DML_RECURRENT_NETWORK_DIRECTION_FORWARD</b>.

