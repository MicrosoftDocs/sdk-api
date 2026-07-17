---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE
tech.root: mf
title: D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE
ms.date: 04/07/2026
targetos: Windows
description: Specifies the bitstream notification mode for a video encode operation.
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
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE
f1_keywords:
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE
 - d3d12video/D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE
---

## -description

Specifies the bitstream notification mode for a video encode operation.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE_FULL_FRAME

The full frame encoding process is used. No subregion notifications are issued.

### -field D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE_SUBREGIONS

Subregion notification mode is enabled. The driver signals fences as individual subregions (for example, slices or tiles) complete, allowing the application to begin consuming results before the entire frame is encoded.

## -remarks

Check for feature support using [D3D12_VIDEO_ENCODER_SUPPORT_FLAGS](ne-d3d12video-d3d12_video_encoder_support_flags.md) before enabling subregion notification mode.

## -see-also

[D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1](ns-d3d12video-d3d12_video_encoder_compressed_bitstream1.md)

[D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM](ns-d3d12video-d3d12_video_encoder_subregion_compressed_bitstream.md)

