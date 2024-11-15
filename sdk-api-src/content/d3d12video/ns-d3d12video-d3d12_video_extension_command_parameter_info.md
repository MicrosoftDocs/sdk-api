---
UID: NS:d3d12video.D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO
title: D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO
ms.date: 11/4/2019
targetos: Windows
description: Describes a video extension command parameter.
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
req.typenames: D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO
f1_keywords:
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO
 - d3d12video/D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO
dev_langs:
 - c++
---

## -description

Describes a video extension command parameter.

## -struct-fields

### -field Name

A pointer to a wide string containing the name of the command.

### -field Type

A member of the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE](ne-d3d12video-d3d12_video_extension_command_parameter_type.md) specifying the type of the parameter.

### -field Flags

A member of the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAGS](ne-d3d12video-d3d12_video_extension_command_parameter_flags.md) enumeration specifying the usage of the parameter.

## -remarks

An array of this structure is provided in a [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_PARAMETERS](ns-d3d12video-d3d12_feature_data_video_extension_command_parameters.md) structure returned from a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS](ne-d3d12video-d3d12_feature_video.md).

## -see-also

