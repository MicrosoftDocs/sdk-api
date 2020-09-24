---
UID: NS:directml.DML_MAX_POOLING_OPERATOR_DESC
title: DML_MAX_POOLING_OPERATOR_DESC
description: Describes a DirectML operator that performs a max pooling function across the input tensor (according to kernel sizes, stride sizes, and pad lengths), y = max(x1 + x2 + … x_pool_size).
helpviewer_keywords: ["DML_MAX_POOLING_OPERATOR_DESC","DML_MAX_POOLING_OPERATOR_DESC structure","direct3d12.dml_max_pooling_operator_desc","directml/DML_MAX_POOLING_OPERATOR_DESC"]
old-location: direct3d12\dml_max_pooling_operator_desc.htm
tech.root: directml
ms.assetid: DC500008-619C-425F-A2C4-DE17B984E4F7
ms.date: 12/5/2018
ms.keywords: DML_MAX_POOLING_OPERATOR_DESC, DML_MAX_POOLING_OPERATOR_DESC structure, direct3d12.dml_max_pooling_operator_desc, directml/DML_MAX_POOLING_OPERATOR_DESC
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
 - DML_MAX_POOLING_OPERATOR_DESC
 - directml/DML_MAX_POOLING_OPERATOR_DESC
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
 - DML_MAX_POOLING_OPERATOR_DESC
---

# DML_MAX_POOLING_OPERATOR_DESC structure


## -description

Describes a DirectML operator that performs a max pooling function across the input tensor (according to kernel sizes, stride sizes, and pad lengths), y = max(x1 + x2 + … x_pool_size).

Max pooling consists of computing the max on all values of a subset of the input tensor according to the kernel size, and then downsampling the data into the output tensor Y for further processing.

[DML_MAX_POOLING1_OPERATOR_DESC](./ns-directml-dml_max_pooling1_operator_desc.md) is an updated version of **DML_MAX_POOLING_OPERATOR_DESC**.

## -struct-fields

### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from. This tensor's dimensions for the image case are [N, C, H, W], where N is the batch size, C is the number of channels, and H and W are the height and the width of the data. For the non-image case, the dimensions are in the form of [N, C, D1, D2, ..., Dn], where N is the batch size.

### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.

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

* [DML_MAX_POOLING1_OPERATOR_DESC](./ns-directml-dml_max_pooling1_operator_desc.md)