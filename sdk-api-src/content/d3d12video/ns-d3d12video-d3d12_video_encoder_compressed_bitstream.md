---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM
tech.root: mf
title: D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM
ms.date: 07/01/2021
targetos: Windows
description: Encapsulates the compressed bitstream output for the encoding operation.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM
f1_keywords:
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM
 - d3d12video/D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM
dev_langs:
 - c++
---

## -description

Encapsulates the compressed bitstream output for the encoding operation.

## -struct-fields

### -field pBuffer

A pointer to a [ID3D12Resource](../d3d12/nn-d3d12-id3d12resource) containing the compressed bitstream buffer. Note that the resource buffer size is not the available size for this encoding operation because *FrameStartOffset* needs to be taken into account against this size.

### -field FrameStartOffset

A UINT64 specifying th offset into the compressed bitstream where the encoder may start adding the current frame output.

## -remarks

The output bitstream is expected to contain the subregion headers, but not the picture, sequence, video or other headers. The host is responsible for coding those headers and generating the complete bitstream.

In subregion frame partitioning, all subregions for a given frame encoding operation output must be placed in top/down, left/right order and must be contiguous.


## -see-also

