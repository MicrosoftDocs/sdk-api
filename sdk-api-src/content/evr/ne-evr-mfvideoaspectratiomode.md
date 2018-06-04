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

# MFVideoAspectRatioMode enumeration


## -description



Specifies the aspect-ratio mode.




## -enum-fields




### -field MFVideoARMode_None

Do not maintain the aspect ratio of the video. Stretch the video to fit the output rectangle.


### -field MFVideoARMode_PreservePicture

Preserve the aspect ratio of the video by letterboxing or within the output rectangle.


### -field MFVideoARMode_PreservePixel

<div class="alert"><b>Note</b>  Currently the EVR ignores this flag.</div>
<div> </div>
Correct the aspect ratio if the physical size of the display device does not match the display resolution. For example, if the native resolution of the monitor is 1600 by 1200 (4:3) but the display resolution is 1280 by 1024 (5:4), the monitor will display non-square pixels.

If this flag is set, you must also set the <b>MFVideoARMode_PreservePicture</b> flag.


### -field MFVideoARMode_NonLinearStretch

Apply a non-linear horizontal stretch if the aspect ratio of the destination rectangle does not match the aspect ratio of the source rectangle.

The non-linear stretch algorithm preserves the aspect ratio in the middle of the picture and stretches (or shrinks) the image progressively more toward the left and right. This mode is useful when viewing 4:3 content full-screen on a 16:9 display, instead of pillar-boxing. Non-linear vertical stretch is not supported, because the visual results are generally poor.

This mode may cause performance degradation.

If this flag is set, you must also set the <b>MFVideoARMode_PreservePixel</b> and <b>MFVideoARMode_PreservePicture</b> flags.


### -field MFVideoARMode_Mask

Bitmask to validate flag values. This value is not a valid flag.


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/b5e81f80-e5c9-4ecf-8f10-d52a0533f086">IMFVideoDisplayControl::GetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/dd49a110-1c11-4eca-9e7b-6021f3bdd397">IMFVideoDisplayControl::SetAspectRatioMode</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

