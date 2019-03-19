---
UID: NE:evr.MFVideoAspectRatioMode
title: MFVideoAspectRatioMode (evr.h)
author: windows-sdk-content
description: Specifies the aspect-ratio mode.
old-location: mf\mfvideoaspectratiomode.htm
tech.root: medfound
ms.assetid: c0a34cff-f86f-4005-9320-5dadfdde5808
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFVideoARMode_Mask, MFVideoARMode_NonLinearStretch, MFVideoARMode_None, MFVideoARMode_PreservePicture, MFVideoARMode_PreservePixel, MFVideoAspectRatioMode, MFVideoAspectRatioMode enumeration [Media Foundation], c0a34cff-f86f-4005-9320-5dadfdde5808, evr/MFVideoARMode_Mask, evr/MFVideoARMode_NonLinearStretch, evr/MFVideoARMode_None, evr/MFVideoARMode_PreservePicture, evr/MFVideoARMode_PreservePixel, evr/MFVideoAspectRatioMode, mf.mfvideoaspectratiomode
ms.topic: enum
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - evr.h
api_name:
 - MFVideoAspectRatioMode
product: Windows
targetos: Windows
req.typenames: MFVideoAspectRatioMode
req.redist: 
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
 

 

