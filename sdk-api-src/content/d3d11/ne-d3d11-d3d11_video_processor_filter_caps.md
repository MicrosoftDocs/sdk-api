---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

