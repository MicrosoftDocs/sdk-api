---
UID: NE:d3d12video.D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE
title: D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE
ms.date: 11/4/2019
targetos: Windows
description: Specifies the types of parameters for video extension commands.
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
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE
f1_keywords:
 - D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE
 - d3d12video/D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE
dev_langs:
 - c++
---

## -description

Specifies the types of parameters for video extension commands.

## -enum-fields

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_UINT8:0

Unsigned 8-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_UINT16:1

Unsigned 16-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_UINT32:2

Unsigned 32-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_UINT64:3

Unsigned 64-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_SINT8:4

Signed 8-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_SINT16:5

Signed 16-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_SINT32:6

Signed 32-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_SINT64:7

Signed 64-bit integer.

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_FLOAT:8

IEEE 32-bit floating point number

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_DOUBLE:9

IEEE 64-bit floating point number

### -field D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_TYPE_RESOURCE:10

A D3D12DDI_HRESOURCE handle.  The caller must use resource barriers to transition to the state appropriate for the parameter.

| D3D12_COMMAND_LIST_SUPPORT_FLAGS value        | Read                      | Write                  |
|-------------------|---------------------------|------------------------|
| D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_DECODE | D3D12_RESOURCE_STATE_VIDEO_DECODE_READ | D3D12_RESOURCE_STATE_VIDEO_DECODE_WRITE |
| D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_PROCESS | D3D12_RESOURCE_STATE_VIDEO_PROCESS_READ | D3D12_RESOURCE_STATE_VIDEO_PROCESS_WRITE |
| D3D12_COMMAND_LIST_SUPPORT_FLAG_VIDEO_ENCODE | D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ | D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE |

## -remarks

Values from this enumeration are used by the [D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](ns-d3d12video-d3d12_video_extension_command_parameter_info.md) structure.

## -see-also

[D3D12_VIDEO_EXTENSION_COMMAND_PARAMETER_INFO](ns-d3d12video-d3d12_video_extension_command_parameter_info.md)

