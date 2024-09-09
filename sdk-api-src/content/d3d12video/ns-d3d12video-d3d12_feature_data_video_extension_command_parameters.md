---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS
title: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS
ms.date: 11/4/2019
targetos: Windows
description: Retrieves the list of video extension command parameters for the specified parameter stage.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS](ne-d3d12video-d3d12_feature_video.md). Retrieves the list of video extension command parameters for the specified parameter stage.

## -struct-fields

### -field CommandId

The unique identifier for the video extension command for which parameters are retrieved.

### -field Stage

A member of the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE](ne-d3d12video-d3d12_video_extension_command_parameter_stage.md) enumeration specifying the parameter stage for which the parameters are retrieved.

### -field ParameterCount

The supported number of video extension command parameters. This value must be the count returned by a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](ne-d3d12video-d3d12_feature_video.md) specified as the feature.

### -field pParameterInfos

Receives a list of [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](ns-d3d12video-d3d12_video_extension_command_parameter_info.md) structures describing video extension command parameters.

## -remarks

## -see-also

