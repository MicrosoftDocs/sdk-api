---
UID: NS:directml.DML_GRU_OPERATOR_DESC
title: DML_GRU_OPERATOR_DESC
description: Performs a (standard layers) one-layer gated recurrent unit (GRU) function on the input. This operator uses multiple gates to perform this layer. These gates are performed multiple times in a loop dictated by the sequence length dimension and the *SequenceLengthsTensor*.
helpviewer_keywords: ["DML_GRU_OPERATOR_DESC","DML_GRU_OPERATOR_DESC structure","direct3d12.dml_gru_operator_desc","directml/DML_GRU_OPERATOR_DESC"]
old-location: direct3d12\dml_gru_operator_desc.htm
tech.root: directml
ms.assetid: 233D9FBC-087D-42B4-84E2-2FDBD6DFF033
ms.date: 05/02/2023
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_GRU_OPERATOR_DESC
 - directml/DML_GRU_OPERATOR_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_GRU_OPERATOR_DESC
---

## -description

Performs a (standard layers) one-layer gated recurrent unit (GRU) function on the input. This operator uses multiple gates to perform this layer. These gates are performed multiple times in a loop dictated by the sequence length dimension and the *SequenceLengthsTensor*.

### Equation for the forward direction

![equation for the forward direction](images/gru_forward.png)

### Equation for the backward direction

![equation for the backward direction](images/gru_backward.png)

### Equation legend

![equation legend](images/gru_legend.png)

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the input data, X. Packed (and potentially padded) into one 4D tensor with the *Sizes* of `{ 1, seq_length, batch_size, input_size }`. seq_length is the dimension that is mapped to the index, t. The tensor doesn't support the **DML_TENSOR_FLAG_OWNED_BY_DML** flag.

### -field WeightTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the weight data, W. Concatenation of W_[zrh] and W_B[zrh] (if bidirectional). The tensor has *Sizes* `{ 1, num_directions, 3 * hidden_size, input_size }`. The tensor doesn't support the **DML_TENSOR_FLAG_OWNED_BY_DML** flag.

### -field RecurrenceTensor

Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

A tensor containing the recurrence data, R. Concatenation of R_[zrh] and R_B[zrh] (if bidirectional). The tensor has *Sizes* `{ 1, num_directions, 3 * hidden_size, hidden_size }`. The tensor doesn't support the **DML_TENSOR_FLAG_OWNED_BY_DML** flag.

### -field BiasTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the bias data, B. Concatenation of (W_b[zrh], R_b[zrh]) and (W_Bb[zrh], R_Bb[zrh]) (if bidirectional). The tensor has *Sizes* `{ 1, 1, num_directions, 6 * hidden_size }`. The tensor doesn't support the **DML_TENSOR_FLAG_OWNED_BY_DML** flag.

### -field HiddenInitTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing the hidden node initializer tensor, H_t-1 for the first loop index t. If not specified, then defaults to 0. This tensor has *Sizes* `{ 1, num_directions, batch_size, hidden_size }`. The tensor doesn't support the **DML_TENSOR_FLAG_OWNED_BY_DML** flag.

### -field SequenceLengthsTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor containing an independent seq_length for each element in the batch. If not specified, then all sequences in the batch have length seq_length. This tensor has *Sizes* `{ 1, 1, 1, batch_size }`. The tensor doesn't support the **DML_TENSOR_FLAG_OWNED_BY_DML** flag.

### -field OutputSequenceTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor with which to write the concatenation of all the intermediate output values of the hidden nodes, H_t. This tensor has *Sizes* `{ seq_length, num_directions, batch_size, hidden_size }`. seq_length is mapped to the loop index t.

### -field OutputSingleTensor

Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***

An optional tensor with which to write the last output value of the hidden nodes, H_t. This tensor has *Sizes* `{ 1, num_directions, batch_size, hidden_size }`.

### -field ActivationDescCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the *ActivationDescs* array.

### -field ActivationDescs

Type: \_Field\_size\_(ActivationDescCount) **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***

An array of [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) containing the descriptions of the activation operators, f() and g(). Both f() and g() are defined independently of direction, meaning that if [DML_RECURRENT_NETWORK_DIRECTION_FORWARD](/windows/win32/api/directml/ne-directml-dml_recurrent_network_direction) or **DML_RECURRENT_NETWORK_DIRECTION_BACKWARD** are supplied in *Direction*, then two activations must be provided. If **DML_RECURRENT_NETWORK_DIRECTION_BIDIRECTIONAL** is supplied, then four activations must be provided. For bidirectional, activations must be provided f() and g() for forward followed by f() and g() for backwards.

### -field Direction

Type: **const [DML_RECURRENT_NETWORK_DIRECTION](/windows/win32/api/directml/ne-directml-dml_recurrent_network_direction)\***

The direction of the operator&mdash;forward, backwards, or bidirectional.

### -field LinearBeforeReset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

**TRUE** to specify that, when computing the output of the hidden gate, the linear transformation should be applied before multiplying by the output of the reset gate. Otherwise, **FALSE**.

## Availability
This operator was introduced in `DML_FEATURE_LEVEL_1_0`.

## Tensor constraints
*BiasTensor*, *HiddenInitTensor*, *InputTensor*, *OutputSequenceTensor*, *OutputSingleTensor*, *RecurrenceTensor*, and *WeightTensor* must have the same *DataType*.

## Tensor support
| Tensor | Kind | Supported dimension counts | Supported data types |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Input | 4 | FLOAT32, FLOAT16 |
| WeightTensor | Input | 4 | FLOAT32, FLOAT16 |
| RecurrenceTensor | Input | 4 | FLOAT32, FLOAT16 |
| BiasTensor | Optional input | 4 | FLOAT32, FLOAT16 |
| HiddenInitTensor | Optional input | 4 | FLOAT32, FLOAT16 |
| SequenceLengthsTensor | Optional input | 4 | UINT32 |
| OutputSequenceTensor | Optional output | 4 | FLOAT32, FLOAT16 |
| OutputSingleTensor | Optional output | 4 | FLOAT32, FLOAT16 |
