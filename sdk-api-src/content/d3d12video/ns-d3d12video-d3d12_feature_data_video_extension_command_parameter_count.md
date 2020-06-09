---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT
title: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT
ms.date: 11/4/2019
ms.topic: language-reference
targetos: Windows
description: Retrieves the supported number of parameters for the specified parameter stage.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT
f1_keywords:
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](ne-d3d12video-d3d12_feature_video.md). Retrieves the  number of video extension command parameters for the specified parameter stage.

## -struct-fields

### -field CommandId

The unique identifier for the video extension command for which the parameter count is queried.

### -field Stage

A member of the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md) enumeration specifying the parameter stage for which the parameter count is retrieved.

### -field ParameterCount

Receives the number of parameters in the parameter stage.

### -field ParameterPacking

Receives the parameter packing for the parameter stage.

## -remarks

## -see-also

