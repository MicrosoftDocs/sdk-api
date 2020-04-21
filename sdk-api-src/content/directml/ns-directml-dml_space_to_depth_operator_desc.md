---
UID: NS:directml.DML_SPACE_TO_DEPTH_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH_OPERATOR_DESC
description: Describes a DirectML data reorganization operator that rearranges blocks of spatial data into depth. The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.helpviewer_keywords: ["DML_SPACE_TO_DEPTH_OPERATOR_DESC","DML_SPACE_TO_DEPTH_OPERATOR_DESC structure","direct3d12.dml_space_to_depth_operator_desc","directml/DML_SPACE_TO_DEPTH_OPERATOR_DESC"]
old-location: direct3d12\dml_space_to_depth_operator_desc.htm
tech.root: direct3d12
ms.assetid: 759769E2-A379-4790-82AD-1B9D3B35D616
ms.date: 12/5/2018
ms.keywords: DML_SPACE_TO_DEPTH_OPERATOR_DESC, DML_SPACE_TO_DEPTH_OPERATOR_DESC structure, direct3d12.dml_space_to_depth_operator_desc, directml/DML_SPACE_TO_DEPTH_OPERATOR_DESC
f1_keywords:
- directml/DML_SPACE_TO_DEPTH_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_SPACE_TO_DEPTH_OPERATOR_DESC structure


## -description






Describes a DirectML data reorganization operator that rearranges blocks of spatial data into depth. The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.

This is the reverse transformation of [DML_DEPTH_TO_SPACE_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_depth_to_space_operator_desc).


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from. The input tensor's dimensions are [N,C,H,W], where N is the batch axis, C is the channel or depth, H is the height, and W is the width.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to. The output tensor's dimensions are [N, C * (<i>BlockSize</i> * <i>BlockSize</i>), H / <i>BlockSize</i>, W / <i>BlockSize</i>].


### -field BlockSize

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

Blocks of [<i>BlockSize</i>, <i>BlockSize</i>] are moved.


## -see-also




[DML_DEPTH_TO_SPACE_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_depth_to_space_operator_desc)
 

 

