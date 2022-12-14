---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_INTRA_REFRESH
tech.root: mf
title: D3D12_VIDEO_ENCODER_INTRA_REFRESH
ms.date: 06/10/2021
targetos: Windows
description: Represents intra refresh settings for video encoding.
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
req.typenames: D3D12_VIDEO_ENCODER_INTRA_REFRESH
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_INTRA_REFRESH
f1_keywords:
 - D3D12_VIDEO_ENCODER_INTRA_REFRESH
 - d3d12video/D3D12_VIDEO_ENCODER_INTRA_REFRESH
dev_langs:
 - c++
---

## -description

Represents intra refresh settings for video encoding.

## -struct-fields

### -field Mode

A value from the [D3D12_VIDEO_ENCODER_INTRA_REFRESH_MODE](ne-d3d12video-d3d12_video_encoder_intra_refresh_mode.md) enumeration specifying the intra refresh mode.

### -field IntraRefreshDuration

A UINT64 specifying the duration of the intra-refresh session, as a number of frames . For D3D12_VIDEO_ENCODER_INTRA_REFRESH_MODE_ROW_BASED, this value and the frame height define the size of the I rows for the duration of the IR session.

## -remarks

When triggering an intra-refresh session, the host informs the current frame number relative to the [0..*IntraRefreshDuration*) session by setting *IntraRefreshFrameIndex* in the picture control structures.


## -see-also

