---
UID: NF:segment.IMSVidVideoRenderer.put__MixerBitmap
title: IMSVidVideoRenderer::put__MixerBitmap (segment.h)
description: The put__MixerBitmap method specifies the static bitmap image.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put__MixerBitmap method","IMSVidVideoRenderer.put__MixerBitmap","IMSVidVideoRenderer::put__MixerBitmap","IMSVidVideoRendererput__MixerBitmap","mstv.imsvidvideorenderer_put__mixerbitmap","put__MixerBitmap","put__MixerBitmap method [Microsoft TV Technologies]","put__MixerBitmap method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put__MixerBitmap"]
old-location: mstv\imsvidvideorenderer_put__mixerbitmap.htm
tech.root: mstv
ms.assetid: 6dd7b83e-6ed6-4c57-8a00-a4ed2c78840d
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put__MixerBitmap method, IMSVidVideoRenderer.put__MixerBitmap, IMSVidVideoRenderer::put__MixerBitmap, IMSVidVideoRendererput__MixerBitmap, mstv.imsvidvideorenderer_put__mixerbitmap, put__MixerBitmap, put__MixerBitmap method [Microsoft TV Technologies], put__MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put__MixerBitmap
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
 - IMSVidVideoRenderer::put__MixerBitmap
 - segment/IMSVidVideoRenderer::put__MixerBitmap
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
 - IMSVidVideoRenderer.put__MixerBitmap
---

# IMSVidVideoRenderer::put__MixerBitmap


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put__MixerBitmap</b> method specifies the static bitmap image.

## -parameters

### -param MixerPicture [in]

A pointer to a <a href="/previous-versions/ms788081(v=vs.85)">VMRALPHABITMAP</a> structure that contains information about the bitmap.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__mixerbitmap">IMSVidVideoRenderer::get__MixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmap">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="/previous-versions/windows/desktop/mstv/mixing-an-image-onto-the-video-window-in-c-">Mixing an Image Onto the Video Window in C++</a>