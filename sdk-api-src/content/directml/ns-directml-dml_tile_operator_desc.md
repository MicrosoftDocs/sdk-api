---
UID: NS:directml.DML_TILE_OPERATOR_DESC
title: DML_TILE_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML data reorganization operator that constructs an output tensor by tiling the input tensor.
old-location: direct3d12\dml_tile_operator_desc.htm
tech.root: direct3d12
ms.assetid: 98D39D8F-4165-4642-B139-EE7417403FCA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_TILE_OPERATOR_DESC, DML_TILE_OPERATOR_DESC structure, direct3d12.dml_tile_operator_desc, directml/DML_TILE_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_TILE_OPERATOR_DESC"
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
 - DML_TILE_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_TILE_OPERATOR_DESC structure


## -description






Describes a DirectML data reorganization operator that constructs  an output tensor by tiling the input tensor.

For example, InputTensor = [[1, 2], [3, 4]], Repeats = [1, 2], gives OutputTensor = [[1, 2, 1, 2], [3, 4, 3, 4]].


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from; this can be of any shape.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to. This tensor is of the same dimension and type as the input tensor. Output_dim[i] = input_dim[i] * repeats[i].


### -field RepeatsCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

This field determines the size of the <i>Repeats</i> array.


### -field Repeats

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

Each value in this array corresponds to one of the input tensor's dimensions (in order). Each value is the number of tiled copies to make of that dimension.

