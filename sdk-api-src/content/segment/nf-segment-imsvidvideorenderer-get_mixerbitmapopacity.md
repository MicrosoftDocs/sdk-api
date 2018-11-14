---
UID: NF:segment.IMSVidVideoRenderer.get_MixerBitmapOpacity
title: IMSVidVideoRenderer::get_MixerBitmapOpacity
author: windows-sdk-content
description: The get_MixerBitmapOpacity method retrieves the opacity of the static bitmap image.
old-location: mstv\imsvidvideorenderer_get_mixerbitmapopacity.htm
tech.root: MSTV
ms.assetid: 830eff1a-e70e-440c-81be-69058d14f314
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MixerBitmapOpacity method, IMSVidVideoRenderer.get_MixerBitmapOpacity, IMSVidVideoRenderer::get_MixerBitmapOpacity, IMSVidVideoRendererget_MixerBitmapOpacity, get_MixerBitmapOpacity, get_MixerBitmapOpacity method [Microsoft TV Technologies], get_MixerBitmapOpacity method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_mixerbitmapopacity, segment/IMSVidVideoRenderer::get_MixerBitmapOpacity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.get_MixerBitmapOpacity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- segment.h
: 
- IMSVidVideoRenderer.get_MixerBitmapOpacity
: 
---

# IMSVidVideoRenderer::get_MixerBitmapOpacity


## -description


The <b>get_MixerBitmapOpacity</b> method retrieves the opacity of the static bitmap image.


## -parameters




### -param opacity

TBD




#### - pOpacity [out]

Receives the opacity, expressed as an integer from 0 (transparent) to 100 (opaque).


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the static bitmap image is set, the VMR alpha-blends the bitmap onto the video image, using the opacity given in <i>pOpacity</i>.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/cfcfab14-7084-4716-8955-574168cd3506">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="https://msdn.microsoft.com/5dba67ab-9522-48a3-be09-8ed8c27bffee">IMSVidVideoRenderer::put_MixerBitmapOpacity</a>
 

 

