---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC
tech.root: mf
title: D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC
ms.date: 06/29/2021
targetos: Windows
description: Represents a reference picture descriptor for HEVC video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC
f1_keywords:
 - D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC
 - d3d12video/D3D12_VIDEO_ENCODER_REFERENCE_PICTURE_DESCRIPTOR_HEVC
dev_langs:
 - c++
---

## -description

Represents a reference picture descriptor for HEVC video encoding.

## -struct-fields

### -field ReconstructedPictureResourceIndex

A **UINT** that maps the current reference picture described by this structure to a resource in the [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC.ReferenceFrames](ns-d3d12video-d3d12_video_encoder_picture_control_desc.md) array.

### -field IsRefUsedByCurrentPic

A **BOOL** indicating whether this descriptor entry is being used by the current picture by being indexed from either L0 and/or L1 lists.

### -field IsLongTermReference

A **BOOL** that is set to true when the described reference frame is being used as a long-term reference picture.

### -field PictureOrderCountNumber

A **UINT** specifying the described reference frame display order.

### -field TemporalLayerIndex

A **UINT** specifying the picture layer number in temporal hierarchy. Check for maximum number of layers in [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION_SUPPORT_H264](ns-d3d12video-d3d12_video_encoder_codec_configuration_support_hevc.md).

## -remarks

## -see-also

