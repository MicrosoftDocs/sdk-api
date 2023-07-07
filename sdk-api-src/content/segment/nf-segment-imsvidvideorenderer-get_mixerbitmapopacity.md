---
UID: NF:segment.IMSVidVideoRenderer.get_MixerBitmapOpacity
title: IMSVidVideoRenderer::get_MixerBitmapOpacity (segment.h)
description: The get_MixerBitmapOpacity method retrieves the opacity of the static bitmap image.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_MixerBitmapOpacity method","IMSVidVideoRenderer.get_MixerBitmapOpacity","IMSVidVideoRenderer::get_MixerBitmapOpacity","IMSVidVideoRendererget_MixerBitmapOpacity","get_MixerBitmapOpacity","get_MixerBitmapOpacity method [Microsoft TV Technologies]","get_MixerBitmapOpacity method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_mixerbitmapopacity","segment/IMSVidVideoRenderer::get_MixerBitmapOpacity"]
old-location: mstv\imsvidvideorenderer_get_mixerbitmapopacity.htm
tech.root: mstv
ms.assetid: 830eff1a-e70e-440c-81be-69058d14f314
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MixerBitmapOpacity method, IMSVidVideoRenderer.get_MixerBitmapOpacity, IMSVidVideoRenderer::get_MixerBitmapOpacity, IMSVidVideoRendererget_MixerBitmapOpacity, get_MixerBitmapOpacity, get_MixerBitmapOpacity method [Microsoft TV Technologies], get_MixerBitmapOpacity method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_mixerbitmapopacity, segment/IMSVidVideoRenderer::get_MixerBitmapOpacity
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
 - IMSVidVideoRenderer::get_MixerBitmapOpacity
 - segment/IMSVidVideoRenderer::get_MixerBitmapOpacity
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
 - IMSVidVideoRenderer.get_MixerBitmapOpacity
---

# IMSVidVideoRenderer::get_MixerBitmapOpacity


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MixerBitmapOpacity</b> method retrieves the opacity of the static bitmap image.

## -parameters

### -param opacity [out]

Receives the opacity, expressed as an integer from 0 (transparent) to 100 (opaque).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the static bitmap image is set, the VMR alpha-blends the bitmap onto the video image, using the opacity given in <i>pOpacity</i>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmap">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmapopacity">IMSVidVideoRenderer::put_MixerBitmapOpacity</a>