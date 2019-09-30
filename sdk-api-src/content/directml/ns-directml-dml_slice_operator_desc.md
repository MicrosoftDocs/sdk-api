---
UID: NS:directml.DML_SLICE_OPERATOR_DESC
title: DML_SLICE_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML data reorganization operator that produces a slice of the input tensor along multiple axes.
old-location: direct3d12\dml_slice_operator_desc.htm
tech.root: direct3d12
ms.assetid: 6CB9CF44-B980-42B3-A967-4095AAA088B3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_SLICE_OPERATOR_DESC, DML_SLICE_OPERATOR_DESC structure, direct3d12.dml_slice_operator_desc, directml/DML_SLICE_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_SLICE_OPERATOR_DESC"
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
 - DML_SLICE_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_SLICE_OPERATOR_DESC structure


## -description






Describes a DirectML data reorganization operator that extracts a single subregion (a "slice") of an input tensor.

This operator copies elements from the input tensor in each dimension N starting from the Offset[N], and advancing Strides[N] elements on the input tensor until Sizes[N] elements are copied to the output tensor.

For example a slice with Offsets [0 0 0 10], Sizes [1 1 1 5], and Strides [1 1 1 2] will copy every second element starting at the 10th element of the input tensor, until a total of 5 elements are copied to the output tensor.

## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to extract slices from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the sliced data results to.


### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of dimensions. This field determines the size of the <i>Offsets</i>,  <i>Sizes</i>, and <i>Strides</i> arrays. This value must match the DimensionCount of the input and output tensors.


### -field Offsets

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the starting index of each dimension to slice from the input tensor.


### -field Sizes

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the size of each dimension of the slice, in elements. The values in this array must match the sizes specified in the output tensor.


### -field Strides

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the element strides for each dimension in the slice.

