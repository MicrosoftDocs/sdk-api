---
UID: NE:d3d12video.D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE
title: D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE
ms.date: 11/4/2019
targetos: Windows
description: Specifies the parameter stages for video extension commands.
tech.root: mf
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE
f1_keywords:
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE
 - d3d12video/D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE
dev_langs:
 - c++
---

## -description

Specifies the parameter stages for video extension commands.

## -enum-fields

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_CREATION:0

The parameter stage is in video extension command creation.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_INITIALIZATION:1

The parameter stage is in video extension command initialization.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_EXECUTION:2

The parameter stage is in video extension command execution.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_CAPS_INPUT:3

The parameter stage is input parameters passed to capabilities queries.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_CAPS_OUTPUT:4

The parameter stage is output parameters passed to capabilities queries.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_DEVICE_EXECUTE_INPUT:5

The parameter stage is device execution input.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_STAGE_DEVICE_EXECUTE_OUTPUT:6

The parameter stage is device execution output.

## -remarks

Values from this enumeration are used when querying for video extension parameter information with calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) with the feature specified as [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETERS](ne-d3d12video-d3d12_feature_video.md) or [D3D12_FEATURE_VIDEO_EXTENSION_COMMAND_PARAMETER_COUNT](ne-d3d12video-d3d12_feature_video.md). The results of these parameter queries may be different for different parameter stages.

## -see-also

