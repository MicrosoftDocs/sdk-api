---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_CONFIGURATION
title: D3D12_VIDEO_DECODE_CONFIGURATION
description: Describes the configuration for a video decoder.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_CONFIGURATION","D3D12_VIDEO_DECODE_CONFIGURATION",""]
tech.root: mf
ms.assetid: 5caab68c-7bdb-4344-beab-ca09341459a1
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_CONFIGURATION, D3D12_VIDEO_DECODE_CONFIGURATION,
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
req.typenames: D3D12_VIDEO_DECODE_CONFIGURATION
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_CONFIGURATION
 - d3d12video/D3D12_VIDEO_DECODE_CONFIGURATION
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_CONFIGURATION
---

# D3D12_VIDEO_DECODE_CONFIGURATION structure


## -description

Describes the configuration for a video decoder.

## -struct-fields

### -field DecodeProfile

A GUID identifying the profile for the decoder, such as D3D12\_VIDEO\_DECODE\_PROFILE\_H264 or D3D12\_VIDEO\_DECODE\_PROFILE\_HEVC\_MAIN. For a list of supported GUIDs, see [Direct3D 12 Video GUIDs](/windows/desktop/medfound/direct3d-12-video-guids).

### -field BitstreamEncryption

A member of the [D3D12\_BITSTREAM\_ENCRYPTION\_TYPE](ne-d3d12video-d3d12_bitstream_encryption_type.md) enumeration specifying the type of bitstream encryption.  For no encryption, use D3D12\_BITSTREAM\_ENCRYPTION\_TYPE\_NONE.

### -field InterlaceType

 
A member of the [D3D12\_VIDEO\_FRAME\_CODED\_INTERLACE\_TYPE](ne-d3d12video-d3d12_video_frame_coded_interlace_type.md) enumeration the desired interlace type used by the coded frames.

## -remarks

## -see-also