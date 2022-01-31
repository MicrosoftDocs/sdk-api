---
UID: NE:d3d12video.D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAGS
title: D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAGS
ms.date: 11/4/2019
targetos: Windows
description: Specifies the usage of the associated video extension command parameter.
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
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAGS
f1_keywords:
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAGS
 - d3d12video/D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAGS
dev_langs:
 - c++
---

## -description

Specifies the usage of the associated video extension command parameter.

## -enum-fields

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAG_NONE:0

None. Set for simple data type parameters.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAG_READ:0x1

The resource parameter is read. This flag is for **ID3D12Resource** only and is not valid for simple data type parameters.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_FLAG_WRITE:0x2

The resource parameter is written. This flag is for **ID3D12Resource** only and is not valid for simple data type parameters.

## -remarks

Values from this enumeration are used by the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](ns-d3d12video-d3d12_video_extension_command_parameter_info.md) structure.

## -see-also

