---
UID: NE:d3d12video.D3D12_VIDEO_FRAME_STEREO_FORMAT
title: D3D12_VIDEO_FRAME_STEREO_FORMAT
description: Defines the layout in memory of a stereo 3D video frame.
helpviewer_keywords: ["D3D12_VIDEO_FRAME_STEREO_FORMAT","D3D12_VIDEO_FRAME_STEREO_FORMAT",""]
tech.root: mf
ms.assetid: bc974169-35ed-4ebb-ba1c-d0c3fe56657a
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_FRAME_STEREO_FORMAT, D3D12_VIDEO_FRAME_STEREO_FORMAT,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12_VIDEO_FRAME_STEREO_FORMAT
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_FRAME_STEREO_FORMAT
 - d3d12video/D3D12_VIDEO_FRAME_STEREO_FORMAT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_FRAME_STEREO_FORMAT
---

# D3D12_VIDEO_FRAME_STEREO_FORMAT enumeration


## -description

Defines the layout in memory of a stereo 3D video frame. All drivers that support stereo must support all of the defined formats.

## -enum-fields

### -field D3D12_VIDEO_FRAME_STEREO_FORMAT_NONE 

No stereo format is specified.

### -field D3D12_VIDEO_FRAME_STEREO_FORMAT_MONO 

The sample does not contain stereo data. If the stereo format is not specified, this value is the default.

### -field D3D12_VIDEO_FRAME_STEREO_FORMAT_HORIZONTAL 

Frame 0 and frame 1 are packed side-by-side, as shown in the following diagram.

![Horizontal stereo format showing the frame 0 pixels on the left of a grid of pixels and the frame 1 pixels on the right](./images/stereo_format_horizontal.png)

### -field D3D12_VIDEO_FRAME_STEREO_FORMAT_VERTICAL 

Frame 0 and frame 1 are packed top-to-bottom, as shown in the following diagram.

![Vertical stereo format showing the frame 0 pixels on the top of a grid of pixels and the frame 1 pixels on the bottom](./images/stereo_format_horizontal.png)

### -field D3D12_VIDEO_FRAME_STEREO_FORMAT_SEPARATE 

Frame 0 and frame 1 are placed in separate resources

## -remarks

## -see-also

