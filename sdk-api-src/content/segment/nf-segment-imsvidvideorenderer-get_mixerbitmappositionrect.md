---
UID: NF:segment.IMSVidVideoRenderer.get_MixerBitmapPositionRect
title: IMSVidVideoRenderer::get_MixerBitmapPositionRect (segment.h)
description: The get_MixerBitmapPositionRect method retrieves the position of the static bitmap image, relative to the video window.helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_MixerBitmapPositionRect method","IMSVidVideoRenderer.get_MixerBitmapPositionRect","IMSVidVideoRenderer::get_MixerBitmapPositionRect","IMSVidVideoRendererget_MixerBitmapPositionRect","get_MixerBitmapPositionRect","get_MixerBitmapPositionRect method [Microsoft TV Technologies]","get_MixerBitmapPositionRect method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_mixerbitmappositionrect","segment/IMSVidVideoRenderer::get_MixerBitmapPositionRect"]
old-location: mstv\imsvidvideorenderer_get_mixerbitmappositionrect.htm
tech.root: mstv
ms.assetid: a2270786-5289-4c41-898e-651ed881842b
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MixerBitmapPositionRect method, IMSVidVideoRenderer.get_MixerBitmapPositionRect, IMSVidVideoRenderer::get_MixerBitmapPositionRect, IMSVidVideoRendererget_MixerBitmapPositionRect, get_MixerBitmapPositionRect, get_MixerBitmapPositionRect method [Microsoft TV Technologies], get_MixerBitmapPositionRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_mixerbitmappositionrect, segment/IMSVidVideoRenderer::get_MixerBitmapPositionRect
f1_keywords:
- segment/IMSVidVideoRenderer.get_MixerBitmapPositionRect
dev_langs:
- c++
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
- IMSVidVideoRenderer.get_MixerBitmapPositionRect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer::get_MixerBitmapPositionRect


## -description


The <b>get_MixerBitmapPositionRect</b> method retrieves the position of the static bitmap image, relative to the video window.


## -parameters




### -param rDest [out]

Receives an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the static bitmap image is set, the VMR alpha-blends the bitmap onto the video image, using the position rectangle given in <i>pprDest</i>.

The returned <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmap">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmappositionrect">IMSVidVideoRenderer::put_MixerBitmapPositionRect</a>
 

 

