---
UID: NE:mpconfig._AM_ASPECT_RATIO_MODE
title: "_AM_ASPECT_RATIO_MODE"
author: windows-driver-content
description: Specifies the aspect ratio of a video image in a display window.
old-location: dshow\am_aspect_ratio_mode.htm
old-project: DirectShow
ms.assetid: 4f7c6220-6231-4bb1-aea6-7f1581b04d3a
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: AM_ARMODE_CROP, AM_ARMODE_LETTER_BOX, AM_ARMODE_STRETCHED, AM_ARMODE_STRETCHED_AS_PRIMARY, AM_ASPECT_RATIO_MODE, AM_ASPECT_RATIO_MODE , AM_ASPECT_RATIO_MODE enumeration [DirectShow], AM_ASPECT_RATIO_MODEEnumeration, _AM_ASPECT_RATIO_MODE, dshow.am_aspect_ratio_mode, mpconfig/AM_ARMODE_CROP, mpconfig/AM_ARMODE_LETTER_BOX, mpconfig/AM_ARMODE_STRETCHED, mpconfig/AM_ARMODE_STRETCHED_AS_PRIMARY, mpconfig/AM_ASPECT_RATIO_MODE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mpconfig.h
req.include-header: 
req.target-type: Windows
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
req.typenames: AM_ASPECT_RATIO_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mpconfig.h
api_name:
-	AM_ASPECT_RATIO_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

