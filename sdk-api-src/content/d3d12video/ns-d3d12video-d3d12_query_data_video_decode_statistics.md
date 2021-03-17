---
UID: NS:d3d12video.D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS
title: D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS
description: Represents data for a video decode statistics query invoked by calling ID3D12VideoDecodeCommandList::EndQuery.
helpviewer_keywords: ["D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS","D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS",""]
tech.root: mf
ms.assetid: c5e06029-cab8-4e16-9bdb-c239818a2a63
ms.date: 05/28/2019
ms.keywords: D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS, D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS,
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
req.typenames: D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS
targetos: Windows
f1_keywords:
 - D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS
 - d3d12video/D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS
---

# D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS structure


## -description

Represents data for a video decode statistics query invoked by calling [ID3D12VideoDecodeCommandList::EndQuery](nf-d3d12video-id3d12videodecodecommandlist-endquery.md).

## -struct-fields

### -field Status

A member of the [D3D12_VIDEO_DECODE_STATUS](ne-d3d12video-d3d12_video_decode_status.md) enumeration indicating the video decoding status.

### -field NumMacroblocksAffected

 
If **Status** is not 0, this member contains the accelerator's estimate of the number of super-blocks in the decoded frame that were adversely affected by the reported problem. If the accelerator does not provide an estimate, the value is **D3D12\_VIDEO\_DECODE\_MACROBLOCKS\_AFFECTED\_UNKNOWN** (0xFFFFFFFFFFFFFFFF).

### -field FrameRate

The decode frame rate.

### -field BitRate

When the **Status** returned is [D3D12_VIDEO_DECODE_STATUS_RATE_EXCEEDED](ne-d3d12video-d3d12_video_decode_status.md), this field reports the bitrate that would succeed.  This value may be used to recreate the decoder and try again.  A value of zero here is valid to indicate that the worst case bit rate should be assumed.  

For all other **Status** values, **BitRate** is set to zero.

## -remarks

## -see-also

