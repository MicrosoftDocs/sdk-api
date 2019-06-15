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
f1_keywords: ["directml/DML_SLICE_OPERATOR_DESC"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_SLICE_OPERATOR_DESC structure


## -description






Describes a DirectML data reorganization operator that produces a slice of the input tensor along multiple axes.

The operator uses strides, offsets, and sizes attributes to specify the offset and size of the dimension for each axis in the list of axes. It uses this information to slice the input data tensor. If a negative value is passed for any of the start or end indices, it represents the number of elements before the end of that dimension. If the value passed to offset or (offset+)size is larger than n (the number of elements in the dimension), then it represents n. For slicing to the end of a dimension with unknown size, you should pass the maximum value for  a [UINT](/windows/desktop/winprog/windows-data-types). If you omit an axis, it is set to [0, ..., ndim-1].


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to extract slices from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the sliced data results to.


### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of dimensions. This field determines the size of the <i>Offsets</i>,  <i>Sizes</i>, and <i>Strides</i> arrays.


### -field Offsets

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the starting index of the corresponding axis.


### -field Sizes

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the size of the corresponding axis.


### -field Strides

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

A pointer to a constant array of [UINT](/windows/desktop/winprog/windows-data-types) containing the lengths of the strides of the tensor.

