---
UID: NS:d3d12video.D3D12_VIDEO_DECODER_HEAP_DESC
title: D3D12_VIDEO_DECODER_HEAP_DESC
description: Describes a ID3D12VideoDecoderHeap.
helpviewer_keywords: ["D3D12_VIDEO_DECODER_HEAP_DESC","D3D12_VIDEO_DECODER_HEAP_DESC",""]
tech.root: mf
ms.assetid: c7a67ba0-08c0-46d2-84c8-ec5d3b127b89
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODER_HEAP_DESC, D3D12_VIDEO_DECODER_HEAP_DESC,
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
req.typenames: D3D12_VIDEO_DECODER_HEAP_DESC
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODER_HEAP_DESC
 - d3d12video/D3D12_VIDEO_DECODER_HEAP_DESC
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODER_HEAP_DESC
---

# D3D12_VIDEO_DECODER_HEAP_DESC structure


## -description

Describes a [ID3D12VideoDecoderHeap](nn-d3d12video-id3d12videodecoderheap.md). Pass this structure into [ID3D12VideoDevice::CreateVideoDecoderHeap](nf-d3d12video-id3d12videodevice-createvideodecoderheap.md) to create an instance of **ID3D12VideoDecoderHeap**.

## -struct-fields

### -field NodeMask

The node mask specifying the physical adapter on which the video processor will be used. For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node, i.e. the device's physical adapter, to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Configuration

A [D3D12_VIDEO_DECODE_CONFIGURATION](ns-d3d12video-d3d12_video_decode_configuration.md) structure specifying the configuration of the video decoder.

### -field DecodeWidth

The decode width of the bitstream to be decoded.

### -field DecodeHeight

The decode height of the bitstream to be decoded.

### -field Format

A [DXGI_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) structure specifying the format of the bitstream to be decoded.

### -field FrameRate

The frame rate of the input video stream.  For more information, see the Remarks section.

### -field BitRate

The average bits per second data compression rate for the compressed video stream.  For more information, see the Remarks section.

### -field MaxDecodePictureBufferCount

 
The maximum number of decode picture buffers this stream can have.

## -remarks

The *BitRate* and *FrameRate* parameters may be used by drivers to inform heuristics such as intermediate allocation sizes.  Decoding a frame may fail if these values are insufficient for the video stream.  Use [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](ns-d3d12video-d3d12_query_data_video_decode_statistics.md) to determine if the video decode succeeded.  If decode fails due to insufficient *BitRate* and *FrameRate* parameters, the *Status* field of this query is set to [D3D12_VIDEO_DECODE_STATUS_RATE_EXCEEDED](ne-d3d12video-d3d12_video_decode_status.md).  This query also returns new *BitRate* and *FrameRate* values that would succeed.

The *BitRate* and *FrameRate* parameters may also be set to zero.  Drivers make worst-case assumptions when these values are used which may result in higher memory consumption with some adapters.

## -see-also