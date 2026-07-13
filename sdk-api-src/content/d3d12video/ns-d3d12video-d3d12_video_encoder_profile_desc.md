---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_PROFILE_DESC
tech.root: mf
title: D3D12_VIDEO_ENCODER_PROFILE_DESC
ms.date: 06/02/2021
targetos: Windows
description: Describes an encoder profile.
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
req.typenames: D3D12_VIDEO_ENCODER_PROFILE_DESC
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_PROFILE_DESC
f1_keywords:
 - D3D12_VIDEO_ENCODER_PROFILE_DESC
 - d3d12video/D3D12_VIDEO_ENCODER_PROFILE_DESC
dev_langs:
 - c++
---

## -description

Describes an encoder profile.

## -struct-fields

### -field DataSize

The data size of the provided encoder profile value.

### -field pH264Profile

A pointer to a value from the [D3D12_VIDEO_ENCODER_PROFILE_H264](ne-d3d12video-d3d12_video_encoder_profile_h264.md) enumeration specifying an H.264 profile.

### -field pHEVCProfile

A pointer to a value from the [D3D12_VIDEO_ENCODER_PROFILE_HEVC](ne-d3d12video-d3d12_video_encoder_profile_hevc.md) enumeration specifying an HEVC profile.

## -remarks


## -see-also

