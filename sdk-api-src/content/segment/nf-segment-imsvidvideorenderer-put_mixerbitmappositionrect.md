---
UID: NF:segment.IMSVidVideoRenderer.put_MixerBitmapPositionRect
title: IMSVidVideoRenderer::put_MixerBitmapPositionRect (segment.h)
description: The put_MixerBitmapPositionRect method specifies the position of the static bitmap image, relative to the video window.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_MixerBitmapPositionRect method","IMSVidVideoRenderer.put_MixerBitmapPositionRect","IMSVidVideoRenderer::put_MixerBitmapPositionRect","IMSVidVideoRendererput_MixerBitmapPositionRect","mstv.imsvidvideorenderer_put_mixerbitmappositionrect","put_MixerBitmapPositionRect","put_MixerBitmapPositionRect method [Microsoft TV Technologies]","put_MixerBitmapPositionRect method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_MixerBitmapPositionRect"]
old-location: mstv\imsvidvideorenderer_put_mixerbitmappositionrect.htm
tech.root: mstv
ms.assetid: 05542d75-1723-4581-ac8b-6a577e0085cb
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_MixerBitmapPositionRect method, IMSVidVideoRenderer.put_MixerBitmapPositionRect, IMSVidVideoRenderer::put_MixerBitmapPositionRect, IMSVidVideoRendererput_MixerBitmapPositionRect, mstv.imsvidvideorenderer_put_mixerbitmappositionrect, put_MixerBitmapPositionRect, put_MixerBitmapPositionRect method [Microsoft TV Technologies], put_MixerBitmapPositionRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_MixerBitmapPositionRect
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidVideoRenderer::put_MixerBitmapPositionRect
 - segment/IMSVidVideoRenderer::put_MixerBitmapPositionRect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidVideoRenderer.put_MixerBitmapPositionRect
---

# IMSVidVideoRenderer::put_MixerBitmapPositionRect


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MixerBitmapPositionRect</b> method specifies the position of the static bitmap image, relative to the video window.

## -parameters

### -param rDest [in]

Pointer to an <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface, specifying the rectangle.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the static bitmap image is set, the VMR alpha blends the bitmap onto the video image, using the specified position rectangle.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-setupmixerbitmap">IMSVidVideoRenderer::SetupMixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmappositionrect">IMSVidVideoRenderer::get_MixerBitmapPositionRect</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmap">IMSVidVideoRenderer::put_MixerBitmap</a>