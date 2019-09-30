---
UID: NS:directml.DML_UPSAMPLE_2D_OPERATOR_DESC
title: DML_UPSAMPLE_2D_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML imaging operator that upsamples the image contained in the input tensor. Each dimension value of the output tensor is output_dimension = floor(input_dimension * scale).
old-location: direct3d12\dml_upsample_2d_operator_desc.htm
tech.root: direct3d12
ms.assetid: 45CA3670-DD38-4617-BF97-CC4133A9FD6D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_UPSAMPLE_2D_OPERATOR_DESC, DML_UPSAMPLE_2D_OPERATOR_DESC structure, direct3d12.dml_upsample_2d_operator_desc, directml/DML_UPSAMPLE_2D_OPERATOR_DESC
ms.topic: struct
f1_keywords: 
 - "directml/DML_UPSAMPLE_2D_OPERATOR_DESC"
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
 - DML_UPSAMPLE_2D_OPERATOR_DESC
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_UPSAMPLE_2D_OPERATOR_DESC structure


## -description






Describes a DirectML imaging operator that upsamples the image contained in the  input tensor. Each dimension value of the output tensor is output_dimension = floor(input_dimension * scale).


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from.


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to.


### -field ScaleSize

Type: [**DML_SIZE_2D**](/windows/desktop/api/directml/ns-directml-dml_size_2d)

The value to scale by, as a 2-D size.


### -field InterpolationMode

Type: [**DML_INTERPOLATION_MODE**](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode)

The interpolation mode to use for the upsample. You can use the default value of [DML_INTERPOLATION_MODE_NEAREST_NEIGHBOR](/windows/desktop/api/directml/ne-directml-dml_interpolation_mode).

