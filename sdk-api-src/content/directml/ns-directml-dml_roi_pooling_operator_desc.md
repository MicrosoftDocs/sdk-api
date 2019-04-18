---
UID: NS:directml.DML_ROI_POOLING_OPERATOR_DESC
title: DML_ROI_POOLING_OPERATOR_DESC
author: windows-sdk-content
description: Describes a DirectML operator that performs a pooling function across the input tensor (according to regions of interest, or ROIs).
old-location: direct3d12\dml_roi_pooling_operator_desc.htm
tech.root: direct3d12
ms.assetid: 7A165306-AC29-4C80-9586-2FB37E85147E
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_ROI_POOLING_OPERATOR_DESC, DML_ROI_POOLING_OPERATOR_DESC structure, direct3d12.dml_roi_pooling_operator_desc, directml/DML_ROI_POOLING_OPERATOR_DESC
ms.topic: struct
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
 - DML_ROI_POOLING_OPERATOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_ROI_POOLING_OPERATOR_DESC structure


## -description






Describes a DirectML operator that performs a pooling function across the input tensor (according to regions of interest, or ROIs).


## -struct-fields




### -field InputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to read from. This tensor's dimensions are [N, C, H, W], where N is the batch size, C is the number of channels, and H and W are the height and the width of the data.


### -field ROITensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the regions of interest (ROIs) to pool over. This tensor is a 2-D tensor of shape (num_rois, 5) given as [[batch_id, x1, y1, x2, y2], ...].


### -field OutputTensor

Type: **const [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc)\***

A pointer to a constant [DML_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_tensor_desc) containing the description of the tensor to write the results to. This tensor is the ROI-pooled output; a 4-D tensor of shape (num_rois, channels, pooled_size[0], pooled_size[1]).


### -field SpatialScale

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a></b>

Multiplicative spatial scale factor, used to translate the ROI coordinates from their input scale to the scale used when pooling. You can use a default value of 1.0.


### -field PooledSize

Type: [**DML_SIZE_2D**](/windows/desktop/api/directml/ns-directml-dml_size_2d)

The ROI pool output size (height, width).

