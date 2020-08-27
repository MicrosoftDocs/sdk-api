---
UID: NS:directml.DML_MAX_POOLING1_OPERATOR_DESC
title: DML_MAX_POOLING1_OPERATOR_DESC
description: Describes a DirectML operator that performs a max pooling function across the input tensor (according to kernel sizes, stride sizes, and pad lengths).
tech.root: directml
ms.date: 01/31/2020
dev_langs:
- c++
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
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
api_name:
 - DML_MAX_POOLING1_OPERATOR_DESC
f1_keywords:
 - directml/DML_MAX_POOLING1_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Describes a DirectML operator that performs a max pooling function across the input tensor (according to kernel sizes, stride sizes, and pad lengths), y = max(x1 + x2 + … x_pool_size). 

Max pooling consists of computing the max on all values of a subset of the input tensor according to the kernel size, and then downsampling the data into the output tensor Y for further processing.

**DML_MAX_POOLING1_OPERATOR_DESC** is an updated version of [DML_MAX_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling_operator_desc).

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from. This tensor's dimensions for the image case are [N, C, H, W], where N is the batch size, C is the number of channels, and H and W are the height and the width of the data. For the non-image case, the dimensions are in the form of [N, C, D1, D2, ..., Dn], where N is the batch size.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

### -field OutputIndicesTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

An optional pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the output indices. The output indices state which maximal element from *InputTensor* was written to *OutputTensor*, where the indices are zero-based in terms of *InputTensor*, treated as if *InputTensor* were one large contiguous 1D array. Both *OutputTensor* and *OutputIndicesTensor* have the same size.

For example, given the input `[[3,5,7,1]],[9,4,2,8]]` where the input indices are implicitly `[0,1,2,3,4,5,6,7]`, and with a pooling size of `3x1`, the output values would be `[[7,7],[9,8]]`, and the output indices would be `[[2,2],[4,7]]`. In `[[7,7],[4,7]]`, the `7` comes from index 2, the `9` comes from index 4, and the `8` comes from index 7.

### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of dimensions. This field determines the size of the <i>Strides</i>,  <i>WindowSize</i>, <i>StartPadding</i>, and <i>EndPadding</i> arrays.

### -field Strides

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the lengths of the strides of the tensor.

### -field WindowSize

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the lengths of the pooling windows.

### -field StartPadding

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the padding (number of pixels added) to the start of the corresponding axis. Padding defaults to 0 along the start and end of each axis.

### -field EndPadding

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the padding (number of pixels added) to the end of the corresponding axis. Padding defaults to 0 along the start and end of each axis.

## -see-also

* [DML_MAX_POOLING_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_max_pooling_operator_desc)
