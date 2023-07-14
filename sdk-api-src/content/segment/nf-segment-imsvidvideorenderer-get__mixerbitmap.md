---
UID: NF:segment.IMSVidVideoRenderer.get__MixerBitmap
title: IMSVidVideoRenderer::get__MixerBitmap (segment.h)
description: The get__MixerBitmap method retrieves the Video Mixing Renderer's IVMRMixerBitmap interface, which controls how the VMR mixes a static bitmap.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get__MixerBitmap method","IMSVidVideoRenderer.get__MixerBitmap","IMSVidVideoRenderer::get__MixerBitmap","IMSVidVideoRendererget__MixerBitmap","get__MixerBitmap","get__MixerBitmap method [Microsoft TV Technologies]","get__MixerBitmap method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get__mixerbitmap","segment/IMSVidVideoRenderer::get__MixerBitmap"]
old-location: mstv\imsvidvideorenderer_get__mixerbitmap.htm
tech.root: mstv
ms.assetid: 714b8222-ab8b-4ece-8ae5-61bb41a7ed3c
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get__MixerBitmap method, IMSVidVideoRenderer.get__MixerBitmap, IMSVidVideoRenderer::get__MixerBitmap, IMSVidVideoRendererget__MixerBitmap, get__MixerBitmap, get__MixerBitmap method [Microsoft TV Technologies], get__MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get__mixerbitmap, segment/IMSVidVideoRenderer::get__MixerBitmap
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
 - IMSVidVideoRenderer::get__MixerBitmap
 - segment/IMSVidVideoRenderer::get__MixerBitmap
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
 - IMSVidVideoRenderer.get__MixerBitmap
---

# IMSVidVideoRenderer::get__MixerBitmap


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__MixerBitmap</b> method retrieves the Video Mixing Renderer's <a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap</a> interface, which controls how the VMR mixes a static bitmap.

## -parameters

### -param MixerPicture [out]

Receives an <a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap</a> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The returned <a href="/windows/win32/api/strmif/nn-strmif-ivmrmixerbitmap">IVMRMixerBitmap</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmap">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__mixerbitmap">IMSVidVideoRenderer::put__MixerBitmap</a>



<a href="/previous-versions/windows/desktop/mstv/mixing-an-image-onto-the-video-window-in-c-">Mixing an Image Onto the Video Window in C++</a>