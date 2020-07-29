---
UID: NS:directml.DML_AVERAGE_POOLING_OPERATOR_DESC
title: DML_AVERAGE_POOLING_OPERATOR_DESC
description: Describes a DirectML operator that performs an average pooling function on the input, y = (x1 + x2 + …) / pool_size.
helpviewer_keywords: ["DML_AVERAGE_POOLING_OPERATOR_DESC","DML_AVERAGE_POOLING_OPERATOR_DESC structure","direct3d12.dml_average_pooling_operator_desc","directml/DML_AVERAGE_POOLING_OPERATOR_DESC"]
old-location: direct3d12\dml_average_pooling_operator_desc.htm
tech.root: directml
ms.assetid: 343A104A-208F-4AB9-A1E7-7EC83FB84AC5
ms.date: 12/5/2018
ms.keywords: DML_AVERAGE_POOLING_OPERATOR_DESC, DML_AVERAGE_POOLING_OPERATOR_DESC structure, direct3d12.dml_average_pooling_operator_desc, directml/DML_AVERAGE_POOLING_OPERATOR_DESC
f1_keywords:
- directml/DML_AVERAGE_POOLING_OPERATOR_DESC
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
- DML_AVERAGE_POOLING_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_AVERAGE_POOLING_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs an average pooling function on the input, y = (x1 + x2 + …) / pool_size.


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


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


### -field IncludePadding

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if pad pixels should be included when calculating values for the edges, otherwise <b>FALSE</b>.

