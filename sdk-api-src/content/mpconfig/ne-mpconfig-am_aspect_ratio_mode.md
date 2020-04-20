---
UID: NE:mpconfig._AM_ASPECT_RATIO_MODE
title: AM_ASPECT_RATIO_MODE (mpconfig.h)
description: Specifies the aspect ratio of a video image in a display window.helpviewer_keywords: ["AM_ARMODE_CROP","AM_ARMODE_LETTER_BOX","AM_ARMODE_STRETCHED","AM_ARMODE_STRETCHED_AS_PRIMARY","AM_ASPECT_RATIO_MODE","AM_ASPECT_RATIO_MODE","AM_ASPECT_RATIO_MODE enumeration [DirectShow]","AM_ASPECT_RATIO_MODEEnumeration","dshow.am_aspect_ratio_mode","mpconfig/AM_ARMODE_CROP","mpconfig/AM_ARMODE_LETTER_BOX","mpconfig/AM_ARMODE_STRETCHED","mpconfig/AM_ARMODE_STRETCHED_AS_PRIMARY","mpconfig/AM_ASPECT_RATIO_MODE"]
old-location: dshow\am_aspect_ratio_mode.htm
tech.root: DirectShow
ms.assetid: 4f7c6220-6231-4bb1-aea6-7f1581b04d3a
ms.date: 12/05/2018
ms.keywords: AM_ARMODE_CROP, AM_ARMODE_LETTER_BOX, AM_ARMODE_STRETCHED, AM_ARMODE_STRETCHED_AS_PRIMARY, AM_ASPECT_RATIO_MODE, AM_ASPECT_RATIO_MODE , AM_ASPECT_RATIO_MODE enumeration [DirectShow], AM_ASPECT_RATIO_MODEEnumeration, dshow.am_aspect_ratio_mode, mpconfig/AM_ARMODE_CROP, mpconfig/AM_ARMODE_LETTER_BOX, mpconfig/AM_ARMODE_STRETCHED, mpconfig/AM_ARMODE_STRETCHED_AS_PRIMARY, mpconfig/AM_ASPECT_RATIO_MODE
f1_keywords:
- mpconfig/AM_ASPECT_RATIO_MODE
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mpconfig.h
api_name:
- AM_ASPECT_RATIO_MODE
targetos: Windows
req.typenames: AM_ASPECT_RATIO_MODE
req.redist: 
ms.custom: 19H1
---

# AM_ASPECT_RATIO_MODE enumeration


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getaspectratiomode">IMixerPinConfig::GetAspectRatioMode</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-setaspectratiomode">IMixerPinConfig::SetAspectRatioMode</a>
 

 

