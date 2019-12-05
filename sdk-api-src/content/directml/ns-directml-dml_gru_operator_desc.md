---
UID: NS:directml.DML_GRU_OPERATOR_DESC
title: DML_GRU_OPERATOR_DESC
description: Describes a DirectML deep learning operator that performs a (standard layers) one-layer gated recurrent unit (GRU) function on the input.
old-location: direct3d12\dml_gru_operator_desc.htm
tech.root: direct3d12
ms.assetid: 233D9FBC-087D-42B4-84E2-2FDBD6DFF033
ms.date: 12/5/2018
ms.keywords: DML_GRU_OPERATOR_DESC, DML_GRU_OPERATOR_DESC structure, direct3d12.dml_gru_operator_desc, directml/DML_GRU_OPERATOR_DESC
ms.topic: struct
f1_keywords:
- directml/DML_GRU_OPERATOR_DESC
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

## -description
Describes a DirectML deep learning operator that performs a (standard layers) one-layer gated recurrent unit (GRU) function on the input. This operator uses multiple gates to perform this layer. These gates are performed multiple times in a loop dictated by the sequence length dimension and the *SequenceLengthsTensor* argument.

### Equation for the forward direction
```cpp
for (t = 0; t < seq_length; t++)
{
    $z_t = f(X_t*W_z^T + H_{t-1} * R_z^T + W_{bz} + R_{bz})$
    $r_t = f(X_t*W_r^T + H_{t-1} * R_r^T + W_{br} + R_{br})$

    if (LinearBeforeReset = 0)
        $h_t = g(X_t*W_h^T + (r_t \bigodot H_{t-1}) * R_h^T + W_{bh} + R_{bh})$
    else
        $h_t = g(X_t*W_h^T + (r_t \bigodot (H_{t-1} * R_h^T + R_{bh}) + W_{bh})$

    $H_t = ((1 - z_t) \bigodot h_t) + (z_t \bigodot H_{t-1})$ 
}
```

### Equation for the backward direction
```cpp
for (t = seq_length - 1; t >= 0; t--)
{
    $z_t = f(X_t*W_{Bz}^T + H_{t-1} * R_{Bz}^T + W_{Bbz} + R_{Bbz})$
    $r_t = f(X_t*W_{Br}^T + H_{t-1} * R_{Br}^T + W_{Bbr} + R_{Bbr})$

    if (LinearBeforeReset = 0)
        $h_t = g(X_t*W_{Bh}^T + (r_t \bigodot H_{t-1}) * R_{Bh}^T + W_{Bbh} + R_{Bbh})$
    else
        $h_t = g(X_t*W_{Bh}^T + (r_t \bigodot (H_{t-1} * R_{Bh}^T + R_{Bbh}) + W_{Bbh})$

    $H_t = ((1 - z_t) \bigodot h_t) + (z_t \bigodot H_{t-1})$ 
}
```

### Equation legend

- $t$ current GRU layer index.
- $t-1$ previous GRU layer index. If backwards direction, then it means $t+1$ index but still the previously calculated $t$.
- $T$ signifies that a matrix will be transposed before use.
- $*$ signifies a matrix multiplication.
- $+$ signifies an element-wise addition of two matrices.
- $\bigodot$ signifies an element-wise multiply of two matrices.
- $H_t$ output of current GRU index $t$.
- $f(),g()$ activation functions dictated by *ActivationDescs*.
- $X_t$ Sub-matrix of the *InputTensor*, which is defined by matrix size [1, batch_size, input_size], at index $t$ of the seq_length dimension.
- $W_{[zrh]}^T$ Forward sub-matrix defined in *WeightTensor*, which is defined to be size [1, batch_size, input_size]. This matrix will be transposed before use.
- $W_{B[zrh]}^T$ Backwards sub-matrix defined in *WeightTensor*, which is defined to be size [1, batch_size, input_size]. This matrix will be transposed before use.
- $H_{t-1}$ an intermediate tensor which is defined to be the output of the previous layer. For the first index of $t$, H_{t-1} is replaced with *HiddenInitTensor*. This is defined to be size [1, batch_size, hidden_size]. A different *HiddenInitTensor* sub-matrix is used for each direction.
- $R_{[zrh]}^T$ Forward sub-matrix of *RecurrenceTensor*, which is defined to be size [1, hidden_size, hidden_size]. This matrix will be transposed before use.
- $R_{B[zrh]}^T$ Backwards sub-matrix of *RecurrenceTensor*, which is defined to be size [1, hidden_size, hidden_size]. This matrix will be transposed before use.
- $W_{b[zrh]}$, $R_{b[zrh]}$ are the bias tensors of the weight tensor, and recurrence tensors, which are sub-matrices of *BiasTensor*. This matrix is size [1,hidden_size] and is broadcasted up to the required size which is [1, batch_size, hidden_size].
- $W_{Bb[zrh]}$, $R_{Bb[zrh]}$ are the bias tensors for the backwards direction
- $z_t$ stands for update gate at index $t$.
- $r_t$ stands for reset gate at index $t$.
- $h_t$ stands for hidden gate at index $t$.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from for the input tensor, $X$. Packed (and potentially padded) into one 4-D tensor with the shape of [1, seq_length, batch_size, input_size]. seq_length is the dimension that is mapped to the GRU index, $t$.

### -field WeightTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the weight tensor, $W$. Concatenation of $W_{[zrh]}$ and $W_{B[zrh]}$ (if bidirectional). The tensor has shape [1, num_directions, 3 * hidden_size, input_size].

### -field RecurrenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the recurrence tensor, $R$. Concatenation of $R_{[zrh]}$ and $R_{B[zrh]}$ (if bidirectional). The tensor has shape [1, num_directions, 3 * hidden_size, hidden_size].

### -field BiasTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the bias tensor, $B$. Concatenation of ($W_{b[zrh]}$, $R_{b[zrh]}$) and ($W_{Bb[zrh]}$, $R_{Bb[zrh]}$) (if bidirectional). The tensor has shape [1, 1, num_directions, 6 * hidden_size].

### -field HiddenInitTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the hidden node initializer tensor, $H_{t-1}$ for the first loop index $t$. If not specified, then defaults to 0. This tensor has shape [1, num_directions, batch_size, hidden_size].

### -field SequenceLengthsTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing an independent seq_length for each element in the batch. If not specified, then all sequences in the batch have length seq_length. This tensor has shape [1, 1, 1, batch_size].

### -field OutputSequenceTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the concatenation of all the intermediate output values of the hidden nodes, $H_t$. This tensor has shape [seq_length, num_directions, batch_size, hidden_size]. seq_length is mapped to the loop index $t$.

### -field OutputSingleTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to which to write the last output value of the hidden nodes, $H_t$. This tensor has shape [1, num_directions, batch_size, hidden_size].

### -field ActivationDescCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the *ActivationDescs* array.

### -field ActivationDescs

Type: **const [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc)\***

A pointer to a constant array of [DML_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_operator_desc) containing the descriptions of the activation operators, $f()$ and $g()$. Both $f()$ and $g()$ are defined independently of direction, meaning that if DML_RECURRENT_NETWORK_DIRECTION_FORWARD or DML_RECURRENT_NETWORD_DIRECTION_BACKWARD are defined 2 activations must be provided. If DML_RECURRENT_NETWORK_DIRECTION_BIDIRECTIONAL is defined 4 activations must be provided. For bidirectional, activations must be provided $f()$ and $g()$ for forward followed by $f()$ and $g()$ for backwards.

### -field Direction

Type: **const [DML_RECURRENT_NETWORK_DIRECTION](/windows/desktop/api/directml/ne-directml-dml_recurrent_network_direction)\***

The direction of the operator—forward, backwards, or bidirectional.

### -field LinearBeforeReset

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to specify that, when computing the output of the hidden gate, the linear transformation should be applied before multiplying by the output of the reset gate. Otherwise, <b>FALSE</b>.
