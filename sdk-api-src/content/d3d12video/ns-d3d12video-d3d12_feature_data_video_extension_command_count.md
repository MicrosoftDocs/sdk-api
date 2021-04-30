---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT
title: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT
ms.date: 11/4/2019
targetos: Windows
description: Retrieves the number of video extension commands.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_EXTENSION_COMMAND_COUNT
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_COUNT](ne-d3d12video-d3d12_feature_video.md). Retrieves the supported number of video extension commands.

## -struct-fields

### -field NodeIndex

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field CommandCount

The supported number of video extension commands.

## -remarks

## -see-also

