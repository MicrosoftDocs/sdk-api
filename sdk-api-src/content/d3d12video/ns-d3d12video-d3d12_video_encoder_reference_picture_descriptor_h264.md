---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264
tech.root: mf
title: D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264
ms.date: 06/23/2021
targetos: Windows
description: Represents a reference picture descriptor for H.264 video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264
f1_keywords:
 - D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264
 - d3d12video/D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_H264
dev_langs:
 - c++
---

## -description

Represents a reference picture descriptor for H.264 video encoding.

## -struct-fields

### -field ReconstructedPictureResourceIndex

Maps the current reference picture described by this structure to a resource in the [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC.ReferenceFrames](ns-d3d12video-d3d12_video_encoder_picture_control_desc.md) array.

### -field IsLongTermReference

Set when the described reference frame is being used as a long-term reference picture.

### -field LongTermPictureIdx

If used as a long term reference, indicates the long-term reference index number.

### -field PictureOrderCountNumber

The described reference frame display order.

### -field FrameDecodingOrderNumber

The frame decode order with semantic as indicated by the slice header *frame_num* syntax element associated with the encoded reference picture.

### -field TemporalLayerIndex

Picture layer number in temporal hierarchy. Please check for maximum number of layers in [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264](ns-d3d12video-d3d12_video_encoder_codec_configuration_support_h264.md).

## -remarks

## -see-also

