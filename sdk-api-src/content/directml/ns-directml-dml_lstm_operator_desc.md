---
UID: NS:directml.DML_LSTM_OPERATOR_DESC
title: DML_LSTM_OPERATOR_DESC
description: Describes a DirectML deep learning operator that performs a one-layer long short term memory (LSTM) function on the input.
old-location: direct3d12\dml_lstm_operator_desc.htm
tech.root: direct3d12
ms.assetid: B2225A27-EB5B-46BC-A224-6A07D869C001
ms.date: 12/5/2018
ms.keywords: DML_LSTM_OPERATOR_DESC, DML_LSTM_OPERATOR_DESC structure, direct3d12.dml_lstm_operator_desc, directml/DML_LSTM_OPERATOR_DESC
ms.topic: struct
f1_keywords:
- directml/DML_LSTM_OPERATOR_DESC
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
- DML_LSTM_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Describes a DirectML deep learning operator that performs a one-layer long short term memory (LSTM) function on the input. This operator uses multiple gates to perform this layer. These gates are performed multiple times in a loop, dictated by the sequence length dimension and the *SequenceLengthsTensor* argument.

### Equation for the forward direction
```cpp
for (t = 0; t < seq_length; t++)
{
    $i_t = f(clip(X_t*W_i^T + H_{t-1} * R_i^T + P_i \bigodot C_{t-1} + W_{bi} + R_{bi}))$

    if (CoupleInputAndForget = 0)
        $f_t = f(clip(X_t*W_f^T + H_{t-1} * R_f^T + P_f \bigodot C_{t-1} + W_{bf} + R_{bf}))$
    else
        $f_t = 1.0 - i_t$

    $c_t = g(clip(X_t*W_c^T + H_{t-1} * R_c^T + W_{bc} + R_{bc}))$
    $C_t = f_t \bigodot C_{t-1} + i_t \bigodot c_t$
    $o_t = f(clip(X_t*W_o^T + H_{t-1} * R_o^T + P_o \bigodot C_{t-1} + W_{bo} + R_{bo}))$
    $H_t = o_t \bigodot h(ct)$ 
}
```

### Equation for the backward direction
```cpp
for (t = seq_length - 1; t >= 0; t--)
{
    $i_t = f(clip(X_t*W_{Bi}^T + H_{t-1} * R_{Bi}^T + P_i \bigodot C_{t-1} + W_{Bbi} + R_{Bbi}))$

    if (CoupleInputAndForget = 0)
        $f_t = f(clip(X_t*W_{Bf}^T + H_{t-1} * R_{Bf}^T + P_f \bigodot C_{t-1} + W_{Bbf} + R_{Bbf}))$
    else
        $f_t = 1.0 - i_t$

    $c_t = g(clip(X_t*W_{Bc}^T + H_{t-1} * R_{Bc}^T + W_{Bbc} + R_{Bbc})$
    $C_t = f_t \bigodot C_{t-1} + i_t \bigodot c_t$
    $o_t = f(clip(X_t*W_{Bo}^T + H_{t-1} * R_{Bo}^T + P_o \bigodot C_{t-1} + W_{Bbo} + R_{Bbo}))$
    $H_t = o_t \bigodot h(ct)$ 
}
```

### Equation legend
- $t$ current LSTM layer index.
- $t-1$ previous LSTM layer index. If backwards direction, then it means $t+1$ index but still the previously calculated $t$.
- $T$ signifies that a matrix will be transposed before use.
- $*$ signifies a matrix multiplication.
- $+$ signifies an element-wise addition of two matrices.
- $\bigodot$ signifies an element-wise multiply of two matrices.
- $f(),g(),h()$ activation functions dictated by *ActivationDescs*.
- clip() optional clipping operation, which is controlled by *UseClipThreshold*.
- $X_t$ Sub-matrix of the *InputTensor*, which is defined by matrix size [1, batch_size, input_size], at index $t$ of the seq_length dimension.
- $W_{[iofc]}^T$ Forward sub-matrix defined in *WeightTensor*, which is defined to be size [1, batch_size, input_size]. This matrix will be transposed before use.
- $W_{B[iofc]}^T$ Backwards sub-matrix defined in *WeightTensor*, which is defined to be size [1, batch_size, input_size]. This matrix will be transposed before use.
- $R_{[iofc]}^T$ Forward sub-matrix of *RecurrenceTensor*, which is defined to be size [1, hidden_size, hidden_size]. This matrix will be transposed before use.
- $R_{B[iofc]}^T$ Backwards sub-matrix of *RecurrenceTensor*, which is defined to be size [1, hidden_size, hidden_size]. This matrix will be transposed before use.
- $H_t$ output of current LSTM index $t$.
- $H_{t-1}$ an intermediate tensor that's defined to be the output of the previous layer. For the first index of $t$, - $H_{t-1}$ is replaced with *HiddenInitTensor*. This is defined to be size [1, batch_size, hidden_size]. A different *HiddenInitTensor* sub-matrix is used for each direction.
- $C_t$ is the tensor containing the Cell Memory for index $t$. 
- $C_{t-1}$ an intermediate tensor that's defined to be the Cell Memory of the previous layer. For the first index of $t$, $C_{t-1}$ is replaced with *CellMemoryInitTensor*. This is defined to be size [1, batch_size, hidden_size]. A different *CellMemoryInitTensor* sub-matrix is used for each direction.
- $W_{b[iofc]}$, $R_{b[iofc]}$ are the bias tensors for the weight tensor, and recurrence tensor, which are sub-matrices of *BiasTensor*. These matrices are size [1,hidden_size], and are broadcasted up to the required size, which is [1, batch_size, hidden_size].
- $W_{Bb[iofc]}$, $R_{Bb[iofc]}$ are the bias tensors for the backwards direction.
- $i_t$ stands for input gate at index $t$.
- $o_t$ stands for output gate at index $t$.
- $f_t$ stands for forget gate at index $t$.
- $c_t$ stands for cell gate at index $t$.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from, $X$. Packed (and potentially padded) into one 4-D tensor with the shape of [1, seq_length, batch_size, input_size]. seq_length is the dimension that is mapped to the GRU index, $t$.

### -field WeightTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor for the gates, $W$. Concatenation of $W_{[iofc]}$ and $W_{B[iofc]}$ (if bidirectional). The tensor has shape [1, num_directions, 4 * hidden_size, input_size].

### -field RecurrenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the recurrence weight tensor, $R$. Concatenation of $R_{[iofc]}$ and $R_{B[iofc]}$ (if bidirectional). This tensor has shape [1, num_directions, 4 * hidden_size, hidden_size].

### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias tensor for the input gate, $B$. Concatenation of [$W_{b[iofc]}$, $R_{b[iofc]}$], and [$W_{Bb[iofc]}$, $R_{Bb[iofc]}$] (if bidirectional). This tensor has shape [1, 1, num_directions, 8 * hidden_size]. If not specified, then defaults to 0 bias.

### -field HiddenInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the hidden node initializer tensor, $H_{t-1}$. Contents of this tensor are only used on the first loop index $t$. If not specified, then defaults to 0. This tensor has shape [1, num_directions, batch_size, hidden_size].

### -field CellMemInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the cell initializer tensor, $C_{t-1}$. Contents of this tensor are only used on the first loop index $t$. If not specified, then defaults to 0. This tensor has shape [1, num_directions, batch_size, hidden_size].

### -field SequenceLengthsTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the lengths of the sequences in a batch. If not specified, then all sequences in the batch have length seq_length. This tensor has shape [1, 1, 1, batch_size].

### -field PeepholeTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor for peepholes, $P$. If not specified, then defaults to 0. Concatenation of $P_{[iof]}$ and $P_{B[iof]}$ (if bidirectional). This tensor has shape [1, 1, num_directions, 3 * hidden_size].

### -field OutputSequenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the concatenation of all the intermediate output values of the hidden nodes, $H_t$. This tensor has shape [seq_length, num_directions, batch_size, hidden_size]. seq_length is mapped to the loop index $t$.

### -field OutputSingleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the last output value of the hidden nodes, $H_t$. This tensor has shape [1, num_directions, batch_size, hidden_size].

### -field OutputCellSingleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the last output value of the cell, $C_{t}$. This tensor has shape [1, num_directions, batch_size, hidden_size].

### -field ActivationDescCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the *ActivationDescs* array.

### -field ActivationDescs

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

A pointer to a constant array of [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the descriptions of the activation operators $f()$, $g()$, and $h()$. $f()$, $g()$, and $h()$ are defined independently of direction, meaning that if **DML_RECURRENT_NETWORK_DIRECTION_FORWARD** or **DML_RECURRENT_NETWORD_DIRECTION_BACKWARD** is defined, then 3 activations must be provided. If **DML_RECURRENT_NETWORK_DIRECTION_BIDIRECTIONAL** is defined, then 6 activations must be provided. For bidirectional, activations must be provided $f()$, $g()$, and $h()$ for forward followed by $f()$, $g()$, and $h()$ for backwards.

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
