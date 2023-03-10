---
UID: NS:d3d12video.D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM
title: D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM
description: Represents a compressed bitstream from which video is decoded.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM","D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM",""]
tech.root: mf
ms.assetid: befe1140-c0d9-4313-a067-40c04ce0d703
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM, D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM,
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
req.typenames: D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM
 - d3d12video/D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM
---

# D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM structure


## -description

Represents a compressed bitstream from which video is decoded.

## -struct-fields

### -field pBuffer

A pointer to an [ID3D12Resource](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) representing the source buffer containing the compressed bitstream to decode.

### -field Offset

The offset to the beginning of the first slice.  This offset has alignment requirements based on the tier value of the video decoder. For more information on decoding tiers, see [D3D12_VIDEO_DECODE_TIER](ne-d3d12video-d3d12_video_decode_tier.md).

### -field Size

The size of the subregion of *pBuffer* that contains the bitstream.

## -remarks

## -see-also