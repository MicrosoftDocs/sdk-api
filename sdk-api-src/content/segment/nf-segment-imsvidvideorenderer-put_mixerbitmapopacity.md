---
UID: NF:segment.IMSVidVideoRenderer.put_MixerBitmapOpacity
title: IMSVidVideoRenderer::put_MixerBitmapOpacity (segment.h)
description: The put_MixerBitmapOpacity method specifies the opacity of the static bitmap image.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_MixerBitmapOpacity method","IMSVidVideoRenderer.put_MixerBitmapOpacity","IMSVidVideoRenderer::put_MixerBitmapOpacity","IMSVidVideoRendererput_MixerBitmapOpacity","mstv.imsvidvideorenderer_put_mixerbitmapopacity","put_MixerBitmapOpacity","put_MixerBitmapOpacity method [Microsoft TV Technologies]","put_MixerBitmapOpacity method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_MixerBitmapOpacity"]
old-location: mstv\imsvidvideorenderer_put_mixerbitmapopacity.htm
tech.root: mstv
ms.assetid: 5dba67ab-9522-48a3-be09-8ed8c27bffee
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_MixerBitmapOpacity method, IMSVidVideoRenderer.put_MixerBitmapOpacity, IMSVidVideoRenderer::put_MixerBitmapOpacity, IMSVidVideoRendererput_MixerBitmapOpacity, mstv.imsvidvideorenderer_put_mixerbitmapopacity, put_MixerBitmapOpacity, put_MixerBitmapOpacity method [Microsoft TV Technologies], put_MixerBitmapOpacity method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_MixerBitmapOpacity
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
 - IMSVidVideoRenderer::put_MixerBitmapOpacity
 - segment/IMSVidVideoRenderer::put_MixerBitmapOpacity
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
 - IMSVidVideoRenderer.put_MixerBitmapOpacity
---

# IMSVidVideoRenderer::put_MixerBitmapOpacity


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MixerBitmapOpacity</b> method specifies the opacity of the static bitmap image.

## -parameters

### -param opacity [in]

Specifies the opacity as an integer from 0 (transparent) to 100 (opaque).

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the static bitmap image is set, the VMR alpha blends the bitmap onto the video image, using the specified opacity.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-setupmixerbitmap">IMSVidVideoRenderer::SetupMixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmapopacity">IMSVidVideoRenderer::get_MixerBitmapOpacity</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmap">IMSVidVideoRenderer::put_MixerBitmap</a>