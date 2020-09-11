---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT
title: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: Retrieves video extension command support using command-defined input and output structures.
tech.root: mf
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_SUPPORT
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_SUPPORT](ne-d3d12video-d3d12_feature_video.md). Retrieves video extension command support using command-defined input and output structures.

## -struct-fields

### -field NodeIndex

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field CommandId

The unique identifier for the video extension command for which support is queried.

### -field pInputData

Input data for the capability query allocated by the caller with a size of *InputDataSizeInBytes*.  This struct is enumerable as the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_CAPS_INPUT](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md) parameter stage.

### -field InputDataSizeInBytes

The byte size of the input data allocation.

### -field pOutputData

Output data for the capability query allocated by the caller with a size of *OutputDataSizeInBytes*.  This struct is enumerable as the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_CAPS_OUTPUT](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md) parameter stage.

### -field OutputDataSizeInBytes

The byte size of the output data allocation.

## -remarks

## -see-also

