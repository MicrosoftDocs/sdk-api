---
UID: NS:d3d12video.D3D12_VIDEO_EXTENSION_COMMAND_INFO
title: D3D12_VIDEO_EXTENSION_COMMAND_INFO
ms.date: 11/4/2019
targetos: Windows
description: Describes a video extension command. (D3D12_VIDEO_EXTENSION_COMMAND_INFO)
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
req.typenames: D3D12_VIDEO_EXTENSION_COMMAND_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_EXTENSION_COMMAND_INFO
f1_keywords:
 - D3D12_VIDEO_EXTENSION_COMMAND_INFO
 - d3d12video/D3D12_VIDEO_EXTENSION_COMMAND_INFO
dev_langs:
 - c++
---

## -description

Describes a video extension command.

## -struct-fields

### -field CommandId

The unique identifier for the video extension command.

### -field Name

A pointer to a wide string containing the name of the command.

### -field CommandListSupportFlags

A member of the [D3D12_COMMAND_LIST_SUPPORT_FLAGS](../d3d12/ne-d3d12-d3d12_command_list_support_flags.md) enumeration.  Indicates the video command queue that the video extension targets. Only one value from the enumeration can be set.

## -remarks

An array of this structure is provided in a [D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS](ns-d3d12video-d3d12_feature_data_video_extension_commands.md) structure returned from a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_EXTENSION_COMMANDS](ne-d3d12video-d3d12_feature_video.md).

## -see-also

[D3D12_COMMAND_LIST_SUPPORT_FLAGS](../d3d12/ne-d3d12-d3d12_command_list_support_flags.md)
