---
UID: NF:segment.IMSVidVideoRenderer.get_MaxVidRect
title: IMSVidVideoRenderer::get_MaxVidRect (segment.h)
description: The get_MaxVidRect method retrieves the maximum ideal size of the video rectangle.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_MaxVidRect method","IMSVidVideoRenderer.get_MaxVidRect","IMSVidVideoRenderer::get_MaxVidRect","IMSVidVideoRendererget_MaxVidRect","get_MaxVidRect","get_MaxVidRect method [Microsoft TV Technologies]","get_MaxVidRect method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_maxvidrect","segment/IMSVidVideoRenderer::get_MaxVidRect"]
old-location: mstv\imsvidvideorenderer_get_maxvidrect.htm
tech.root: mstv
ms.assetid: b4c4b2da-0749-463c-aaa1-04d0d456327a
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MaxVidRect method, IMSVidVideoRenderer.get_MaxVidRect, IMSVidVideoRenderer::get_MaxVidRect, IMSVidVideoRendererget_MaxVidRect, get_MaxVidRect, get_MaxVidRect method [Microsoft TV Technologies], get_MaxVidRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_maxvidrect, segment/IMSVidVideoRenderer::get_MaxVidRect
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
 - IMSVidVideoRenderer::get_MaxVidRect
 - segment/IMSVidVideoRenderer::get_MaxVidRect
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
 - IMSVidVideoRenderer.get_MaxVidRect
---

# IMSVidVideoRenderer::get_MaxVidRect


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_MaxVidRect</b> method retrieves the maximum ideal size of the video rectangle.

## -parameters

### -param ppVidRect [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The maximum ideal image size is the maximum video size that can be displayed without significantly degrading performance or image quality.

The returned <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_minvidrect">IMSVidVideoRenderer::get_MinVidRect</a>