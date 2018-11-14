---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_FILTER
title: D3D11_VIDEO_PROCESSOR_FILTER
author: windows-sdk-content
description: Identifies a video processor filter.
old-location: mf\d3d11_video_processor_filter.htm
tech.root: medfound
ms.assetid: 87CF9A1A-E196-4B5A-BAAE-DD948A5468C2
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_FILTER, D3D11_VIDEO_PROCESSOR_FILTER enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING, D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS, D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST, D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT, D3D11_VIDEO_PROCESSOR_FILTER_HUE, D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION, D3D11_VIDEO_PROCESSOR_FILTER_SATURATION, D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT, d3d11/D3D11_VIDEO_PROCESSOR_FILTER, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_HUE, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_SATURATION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT, mf.d3d11_video_processor_filter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_FILTER
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_PROCESSOR_FILTER
req.redist: 
---

# D3D11_VIDEO_PROCESSOR_FILTER enumeration


## -description


Identifies a video processor filter.


## -enum-fields




### -field D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS

Brightness filter.


### -field D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST

Contrast filter.


### -field D3D11_VIDEO_PROCESSOR_FILTER_HUE

Hue filter.


### -field D3D11_VIDEO_PROCESSOR_FILTER_SATURATION

Saturation filter.


### -field D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION

Noise reduction filter.


### -field D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT

Edge enhancement filter.


### -field D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING

Anamorphic scaling filter.


### -field D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT

Stereo adjustment filter. When stereo 3D video is enabled, this filter adjusts the offset between the left and right views, allowing the user to reduce potential eye strain. 

The filter value indicates the amount by which the left and right views are adjusted.  A positive value shifts the images away from each other: the left image toward the left, and the right image toward the right. A negative value shifts the images in the opposite directions, closer to each other.


## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>



<a href="https://msdn.microsoft.com/49258E8F-50BC-4F51-A492-78B44A73CC13">ID3D11VideoContext::VideoProcessorSetStreamFilter</a>
 

 

