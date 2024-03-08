---
UID: NF:segment.IMSVidVideoRenderer.SetupMixerBitmap
title: IMSVidVideoRenderer::SetupMixerBitmap (segment.h)
description: The SetupMixerBitmap method configures the Video Mixing Renderer (VMR) to display an alpha-blended bitmap on top of the video.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","SetupMixerBitmap method","IMSVidVideoRenderer.SetupMixerBitmap","IMSVidVideoRenderer::SetupMixerBitmap","IMSVidVideoRendererSetupMixerBitmap","SetupMixerBitmap","SetupMixerBitmap method [Microsoft TV Technologies]","SetupMixerBitmap method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_setupmixerbitmap","segment/IMSVidVideoRenderer::SetupMixerBitmap"]
old-location: mstv\imsvidvideorenderer_setupmixerbitmap.htm
tech.root: mstv
ms.assetid: a91561e3-469b-412a-b5ab-af2a5a0855a6
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],SetupMixerBitmap method, IMSVidVideoRenderer.SetupMixerBitmap, IMSVidVideoRenderer::SetupMixerBitmap, IMSVidVideoRendererSetupMixerBitmap, SetupMixerBitmap, SetupMixerBitmap method [Microsoft TV Technologies], SetupMixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_setupmixerbitmap, segment/IMSVidVideoRenderer::SetupMixerBitmap
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
 - IMSVidVideoRenderer::SetupMixerBitmap
 - segment/IMSVidVideoRenderer::SetupMixerBitmap
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
 - IMSVidVideoRenderer.SetupMixerBitmap
---

# IMSVidVideoRenderer::SetupMixerBitmap


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>SetupMixerBitmap</b> method configures the Video Mixing Renderer (VMR) to display an alpha-blended bitmap on top of the video.

## -parameters

### -param MixerPictureDisp [in]

Pointer to an <b>IPictureDisp</b> interface that specifies the bitmap.

### -param Opacity [in]

Specifies the opacity of the bitmap, as an integer from 0 (transparent) to 100 (opaque).

### -param rDest [in]

Pointer to an <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface that specifies the position of the bitmap, relative to the video window.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmap">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmapopacity">IMSVidVideoRenderer::put_MixerBitmapOpacity</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmappositionrect">IMSVidVideoRenderer::put_MixerBitmapPositionRect</a>