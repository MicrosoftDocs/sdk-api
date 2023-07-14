---
UID: NF:segment.IMSVidVideoRenderer.get_MinVidRect
title: IMSVidVideoRenderer::get_MinVidRect (segment.h)
description: The get_MinVidRect method retrieves the minimum ideal size of the video rectangle.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_MinVidRect method","IMSVidVideoRenderer.get_MinVidRect","IMSVidVideoRenderer::get_MinVidRect","IMSVidVideoRendererget_MinVidRect","get_MinVidRect","get_MinVidRect method [Microsoft TV Technologies]","get_MinVidRect method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_minvidrect","segment/IMSVidVideoRenderer::get_MinVidRect"]
old-location: mstv\imsvidvideorenderer_get_minvidrect.htm
tech.root: mstv
ms.assetid: 2e65f2b2-d479-429a-b5c7-8c5cbb6c833d
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MinVidRect method, IMSVidVideoRenderer.get_MinVidRect, IMSVidVideoRenderer::get_MinVidRect, IMSVidVideoRendererget_MinVidRect, get_MinVidRect, get_MinVidRect method [Microsoft TV Technologies], get_MinVidRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_minvidrect, segment/IMSVidVideoRenderer::get_MinVidRect
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
 - IMSVidVideoRenderer::get_MinVidRect
 - segment/IMSVidVideoRenderer::get_MinVidRect
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
 - IMSVidVideoRenderer.get_MinVidRect
---

# IMSVidVideoRenderer::get_MinVidRect


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MinVidRect</b> method retrieves the minimum ideal size of the video rectangle.

## -parameters

### -param ppVidRect [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The minimum ideal image size is the minimum video size that can be displayed without significantly degrading performance or image quality.

The returned <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_maxvidrect">IMSVidVideoRenderer::get_MaxVidRect</a>