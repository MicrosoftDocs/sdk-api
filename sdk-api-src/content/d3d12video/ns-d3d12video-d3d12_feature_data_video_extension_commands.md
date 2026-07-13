---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS
title: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS
ms.date: 11/4/2019
targetos: Windows
description: Retrieves the list of video extension commands from the driver.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMANDS
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_EXTENSION_COMMANDS](ne-d3d12video-d3d12_feature_video.md). Retrieves the list of video extension commands from the driver.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, this indicates which physical adapter of the device this operation applies to.

### -field CommandCount

The supported number of video extension commands. This value must be the count returned by a call to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_COUNT](ne-d3d12video-d3d12_feature_video.md) specified as the feature.

### -field pCommandInfos

Receives a list of [D3D12_VIDEO_EXTENSION_COMMAND_INFO](ns-d3d12video-d3d12_video_extension_command_info.md) structures describing video extension commands.

## -remarks

## -see-also

