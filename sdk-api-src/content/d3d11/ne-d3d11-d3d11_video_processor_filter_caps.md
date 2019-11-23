---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_FILTER_CAPS
title: D3D11_VIDEO_PROCESSOR_FILTER_CAPS (d3d11.h)

description: Defines image filter capabilities for a Microsoft Direct3D 11 video processor.
old-location: mf\d3d11_video_processor_filter_caps.htm
tech.root: medfound
ms.assetid: 445C2416-DD81-444B-85E0-1A6249D97EDA

ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_FILTER_CAPS, D3D11_VIDEO_PROCESSOR_FILTER_CAPS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_FILTER_CAPS_ANAMORPHIC_SCALING, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_BRIGHTNESS, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_CONTRAST, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_EDGE_ENHANCEMENT, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_HUE, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_NOISE_REDUCTION, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_SATURATION, D3D11_VIDEO_PROCESSOR_FILTER_CAPS_STEREO_ADJUSTMENT, D3D11_VIDEO_PROCESSPR_FILTER_CAPS, D3D11_VIDEO_PROCESSPR_FILTER_CAPS enumeration [Media Foundation], d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_ANAMORPHIC_SCALING, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_BRIGHTNESS, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_CONTRAST, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_EDGE_ENHANCEMENT, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_HUE, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_NOISE_REDUCTION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_SATURATION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CAPS_STEREO_ADJUSTMENT, mf.d3d11_video_processor_filter_caps, mf.d3d11_video_processpr_filter_caps
ms.topic: enum
f1_keywords: 
 - "d3d11/D3D11_VIDEO_PROCESSPR_FILTER_CAPS"
dev_langs:
 - c++
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
 - D3D11_VIDEO_PROCESSPR_FILTER_CAPS
targetos: Windows
req.typenames: D3D11_VIDEO_PROCESSOR_FILTER_CAPS
req.redist: 
ms.custom: 19H1
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



These capability flags indicate support for the image filters defined by the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_filter">D3D11_VIDEO_PROCESSOR_FILTER</a> enumeration. To apply a particular filter, call the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter">ID3D11VideoContext::VideoProcessorSetStreamFilter</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
 

 

