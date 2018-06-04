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

# _AM_ASPECT_RATIO_MODE enumeration


## -description



Specifies the aspect ratio of a video image in a display window.




## -enum-fields




### -field AM_ARMODE_STRETCHED

No aspect ratio correction.


### -field AM_ARMODE_LETTER_BOX

Put the video in letterbox format. Paint background color in the excess region so the video is not distorted.


### -field AM_ARMODE_CROP

Crop the video to the correct aspect ratio.


### -field AM_ARMODE_STRETCHED_AS_PRIMARY

Use whatever mode is currently set for the primary stream. This value is valid only for secondary streams.


## -remarks



The AM_ARMODE_STRETCHED member causes a video stream to occupy the entire region of the display window when the window is resized, possibly stretching the video. The AM_ARMODE_LETTER_BOX member eliminates video stretching and distortions by keeping the aspect ratio consistent and painting the excess areas of the window a background color. The AM_ARMODE_CROP member also prevents stretching, by cropping the image if necessary.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/091ebea0-8688-4965-8727-0738cc19d47e">IMixerPinConfig::GetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/907ab0cf-c0a4-4e81-8fb4-90914427d9c0">IMixerPinConfig::SetAspectRatioMode</a>
 

 

