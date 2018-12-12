---
UID: NF:segment.IMSVidVideoRenderer.put_MixerBitmapPositionRect
title: IMSVidVideoRenderer::put_MixerBitmapPositionRect
author: windows-sdk-content
description: The put_MixerBitmapPositionRect method specifies the position of the static bitmap image, relative to the video window.
old-location: mstv\imsvidvideorenderer_put_mixerbitmappositionrect.htm
tech.root: mstv
ms.assetid: 05542d75-1723-4581-ac8b-6a577e0085cb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_MixerBitmapPositionRect method, IMSVidVideoRenderer.put_MixerBitmapPositionRect, IMSVidVideoRenderer::put_MixerBitmapPositionRect, IMSVidVideoRendererput_MixerBitmapPositionRect, mstv.imsvidvideorenderer_put_mixerbitmappositionrect, put_MixerBitmapPositionRect, put_MixerBitmapPositionRect method [Microsoft TV Technologies], put_MixerBitmapPositionRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_MixerBitmapPositionRect
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
 - IMSVidVideoRenderer.put_MixerBitmapPositionRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::put_MixerBitmapPositionRect


## -description


The <b>put_MixerBitmapPositionRect</b> method specifies the position of the static bitmap image, relative to the video window.


## -parameters




### -param rDest [in]

Pointer to an <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface, specifying the rectangle.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the static bitmap image is set, the VMR alpha blends the bitmap onto the video image, using the specified position rectangle.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694760(v=VS.85).aspx">IMSVidVideoRenderer::SetupMixerBitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694741(v=VS.85).aspx">IMSVidVideoRenderer::get_MixerBitmapPositionRect</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694751(v=VS.85).aspx">IMSVidVideoRenderer::put_MixerBitmap</a>
 

 

