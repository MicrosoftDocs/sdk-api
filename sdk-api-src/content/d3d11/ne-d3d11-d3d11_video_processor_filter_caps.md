---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_FILTER_CAPS
title: D3D11_VIDEO_PROCESSOR_FILTER_CAPS
author: windows-sdk-content
description: Defines image filter capabilities for a Microsoft Direct3D 11 video processor.
old-location: mf\d3d11_video_processor_filter_caps.htm
old-project: medfound
ms.assetid: 445C2416-DD81-444B-85E0-1A6249D97EDA
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_FILTER_CAPS, D3D11_VIDEO_PROCESSOR_FILTER_CAPS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_FILTER_CAPS_ANAMORPHIC_SCALING, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_BRIGHTNESS, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_CONTRAST, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_EDGE_ENHANCEMENT, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_HUE, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_NOISE_REDUCTION, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_SATURATION, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_STEREO_ADJUSTMENT, D3D11_VIDEO_PROCESSPR_FILTER_CAPS, D3D11_VIDEO_PROCESSPR_FILTER_CAPS enumeration [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_ANAMORPHIC_SCALING, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_BRIGHTNESS, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_CONTRAST, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_EDGE_ENHANCEMENT, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_HUE, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_NOISE_REDUCTION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_SATURATION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_STEREO_ADJUSTMENT, mf.d3d11_video_processor_filter_caps, mf.d3d11_video_processpr_filter_caps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: D3D11_VIDEO_PROCESSOR_FILTER_CAPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSPR_FILTER_CAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_PROCESSOR_FILTER_CAPS enumeration


## -description


Defines image filter capabilities for a Microsoft Direct3D 11 video processor.


## -enum-fields




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_BRIGHTNESS

The video processor can adjust the brightness level.




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_CONTRAST

The video processor can adjust the contrast level.




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_HUE

The video processor can adjust hue.




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_SATURATION

The video processor can adjust the saturation level.




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_NOISE_REDUCTION

The video processor can perform noise reduction.




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_EDGE_ENHANCEMENT

The video processor can perform edge enhancement.




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_ANAMORPHIC_SCALING

The video processor can perform anamorphic scaling. Anamorphic scaling can be used to stretch 4:3 content to a widescreen 16:9 aspect ratio.




### -field D3D11_VIDEO_PROCESSOR_FILTER_CAPS_STEREO_ADJUSTMENT

For stereo 3D video, the video processor can adjust the offset between the left and right views, allowing the user to reduce potential eye strain.


## -remarks



These capability flags indicate support for the image filters defined by the <a href="https://msdn.microsoft.com/87CF9A1A-E196-4B5A-BAAE-DD948A5468C2">D3D11_VIDEO_PROCESSOR_FILTER</a> enumeration. To apply a particular filter, call the <a href="https://msdn.microsoft.com/49258E8F-50BC-4F51-A492-78B44A73CC13">ID3D11VideoContext::VideoProcessorSetStreamFilter</a> method.




## -see-also




<a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a>



<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>
 

 

