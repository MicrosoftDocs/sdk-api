---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE
tech.root: mf
title: D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE
ms.date: 04/07/2026
targetos: Windows
description: Specifies how subregion output buffers are passed in D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE
f1_keywords:
 - D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE
 - d3d12video/D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE
---

## -description

Specifies how subregion output buffers are passed in [D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM](ns-d3d12video-d3d12_video_encoder_subregion_compressed_bitstream.md).

## -enum-fields

### -field D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE_ARRAY_OF_BUFFERS

Each subregion is written to a different [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) buffer object. Requires **D3D12_VIDEO_ENCODER_SUPPORT_FLAG_SUBREGION_NOTIFICATION_AVAILABLE_ARRAY_OF_BUFFERS** support.

### -field D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM_BUFFER_MODE_SINGLE_BUFFER

All subregions are written into the same [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) buffer. The driver partitions the buffer into non-overlapping regions. Requires **D3D12_VIDEO_ENCODER_SUPPORT_FLAG_SUBREGION_NOTIFICATION_AVAILABLE_SINGLE_BUFFER** support.

## -remarks

The associated [ID3D12VideoEncoderHeap](nn-d3d12video-id3d12videoencoderheap.md) must be created with the corresponding [D3D12_VIDEO_ENCODER_HEAP_FLAGS](ne-d3d12video-d3d12_video_encoder_heap_flags.md) flag set.

## -see-also

[D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM](ns-d3d12video-d3d12_video_encoder_subregion_compressed_bitstream.md)

