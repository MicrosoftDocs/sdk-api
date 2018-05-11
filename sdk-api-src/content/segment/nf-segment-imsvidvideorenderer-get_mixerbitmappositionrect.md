---
UID: NF:segment.IMSVidVideoRenderer.get_MixerBitmapPositionRect
title: IMSVidVideoRenderer::get_MixerBitmapPositionRect
author: windows-driver-content
description: The get_MixerBitmapPositionRect method retrieves the position of the static bitmap image, relative to the video window.
old-location: mstv\imsvidvideorenderer_get_mixerbitmappositionrect.htm
old-project: mstv
ms.assetid: a2270786-5289-4c41-898e-651ed881842b
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MixerBitmapPositionRect method, IMSVidVideoRenderer.get_MixerBitmapPositionRect, IMSVidVideoRenderer::get_MixerBitmapPositionRect, IMSVidVideoRendererget_MixerBitmapPositionRect, get_MixerBitmapPositionRect, get_MixerBitmapPositionRect method [Microsoft TV Technologies], get_MixerBitmapPositionRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_mixerbitmappositionrect, segment/IMSVidVideoRenderer::get_MixerBitmapPositionRect
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRenderer.get_MixerBitmapPositionRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRenderer::get_MixerBitmapPositionRect


## -description


The <b>get_MixerBitmapPositionRect</b> method retrieves the position of the static bitmap image, relative to the video window.


## -parameters




### -param rDest






#### - pprDest [out]

Receives an <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the static bitmap image is set, the VMR alpha-blends the bitmap onto the video image, using the position rectangle given in <i>pprDest</i>.

The returned <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/cfcfab14-7084-4716-8955-574168cd3506">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="https://msdn.microsoft.com/05542d75-1723-4581-ac8b-6a577e0085cb">IMSVidVideoRenderer::put_MixerBitmapPositionRect</a>
 

 

