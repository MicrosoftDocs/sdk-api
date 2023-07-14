---
UID: NF:segment.IMSVidVideoRenderer.put_MixerBitmap
title: IMSVidVideoRenderer::put_MixerBitmap (segment.h)
description: The put_MixerBitmap method specifies the static bitmap image, as an IPictureDisp type.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_MixerBitmap method","IMSVidVideoRenderer.put_MixerBitmap","IMSVidVideoRenderer::put_MixerBitmap","IMSVidVideoRendererput_MixerBitmap","mstv.imsvidvideorenderer_put_mixerbitmap","put_MixerBitmap","put_MixerBitmap method [Microsoft TV Technologies]","put_MixerBitmap method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_MixerBitmap"]
old-location: mstv\imsvidvideorenderer_put_mixerbitmap.htm
tech.root: mstv
ms.assetid: fa9d9bea-f711-42f1-a247-322036744c44
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_MixerBitmap method, IMSVidVideoRenderer.put_MixerBitmap, IMSVidVideoRenderer::put_MixerBitmap, IMSVidVideoRendererput_MixerBitmap, mstv.imsvidvideorenderer_put_mixerbitmap, put_MixerBitmap, put_MixerBitmap method [Microsoft TV Technologies], put_MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_MixerBitmap
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
 - IMSVidVideoRenderer::put_MixerBitmap
 - segment/IMSVidVideoRenderer::put_MixerBitmap
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
 - IMSVidVideoRenderer.put_MixerBitmap
---

# IMSVidVideoRenderer::put_MixerBitmap


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MixerBitmap</b> method specifies the static bitmap image, as an <b>IPictureDisp</b> type.

## -parameters

### -param MixerPictureDisp [in]

Specifies a pointer to the <b>IPictureDisp</b> interface.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The VMR alpha-blends the static bitmap image onto the video image. For information about the <b>IPictureDisp</b> interface, see the Platform SDK documentation.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-setupmixerbitmap">IMSVidVideoRenderer::SetupMixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_mixerbitmap">IMSVidVideoRenderer::get_MixerBitmap</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmapopacity">IMSVidVideoRenderer::put_MixerBitmapOpacity</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_mixerbitmappositionrect">IMSVidVideoRenderer::put_MixerBitmapPositionRect</a>



<a href="/previous-versions/windows/desktop/mstv/mixing-an-image-onto-the-video-window-in-c-">Mixing an Image Onto the Video Window in C++</a>