---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1
tech.root: mf
title: D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1
ms.date: 04/07/2026
targetos: Windows
description: Encapsulates the compressed bitstream output for an encoding operation, with support for subregion notification.
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1
f1_keywords:
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1
 - d3d12video/D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1
---

## -description

Encapsulates the compressed bitstream output for an encoding operation, with support for subregion notification.

## -struct-fields

### -field NotificationMode

A [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE](ne-d3d12video-d3d12_video_encoder_compressed_bitstream_notification_mode.md) value that selects between full-frame and subregion notification output modes.

### -field FrameOutputBuffer

A [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM](ns-d3d12video-d3d12_video_encoder_compressed_bitstream.md) for full-frame output. Used when **NotificationMode** is **D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE_FULL_FRAME**.

### -field SubregionOutputBuffers

A [D3D12_VIDEO_ENCODER_SUBREGION_COMPRESSED_BITSTREAM](ns-d3d12video-d3d12_video_encoder_subregion_compressed_bitstream.md) for per-subregion output. Used when **NotificationMode** is **D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM_NOTIFICATION_MODE_SUBREGIONS**.

## -remarks

**FrameOutputBuffer** and **SubregionOutputBuffers** are members of a union. Only the member corresponding to the selected **NotificationMode** is used.

## -see-also

[D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_encodeframe_output_arguments1.md)

