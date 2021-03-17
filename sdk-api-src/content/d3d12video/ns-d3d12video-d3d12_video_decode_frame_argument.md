---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_FRAME_ARGUMENT
title: D3D12_VIDEO_DECODE_FRAME_ARGUMENT
description: Represents the decode parameters for a frame.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_FRAME_ARGUMENT","D3D12_VIDEO_DECODE_FRAME_ARGUMENT",""]
tech.root: mf
ms.assetid: d5e35570-69a6-40a3-bfc6-a7c1e3d8b57d
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_FRAME_ARGUMENT, D3D12_VIDEO_DECODE_FRAME_ARGUMENT,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODE_FRAME_ARGUMENT
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_FRAME_ARGUMENT
 - d3d12video/D3D12_VIDEO_DECODE_FRAME_ARGUMENT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_FRAME_ARGUMENT
---

# D3D12_VIDEO_DECODE_FRAME_ARGUMENT structure


## -description

Represents the decode parameters for a frame. Parameter definitions are specified by the codec specification for each decode profile.

## -struct-fields

### -field Type

A member of the [D3D12_VIDEO_DECODE_ARGUMENT_TYPE](ne-d3d12video-d3d12_video_decode_argument_type.md) enumeration specifying the type of argument.

### -field Size

The size of the data in *pArgument*, in bytes.

### -field pData

 
A pointer to the argument data.

## -remarks

## -see-also

