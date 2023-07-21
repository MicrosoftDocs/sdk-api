---
UID: NF:segment.IMSVidVideoRenderer.get_ClippedSourceRect
title: IMSVidVideoRenderer::get_ClippedSourceRect (segment.h)
description: The get_ClippedSourceRect method retrieves the clipping rectangle on the video source.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_ClippedSourceRect method","IMSVidVideoRenderer.get_ClippedSourceRect","IMSVidVideoRenderer::get_ClippedSourceRect","IMSVidVideoRendererget_ClippedSourceRect","get_ClippedSourceRect","get_ClippedSourceRect method [Microsoft TV Technologies]","get_ClippedSourceRect method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_clippedsourcerect","segment/IMSVidVideoRenderer::get_ClippedSourceRect"]
old-location: mstv\imsvidvideorenderer_get_clippedsourcerect.htm
tech.root: mstv
ms.assetid: d40d39d9-41a4-42e1-b0d0-4a6299fd1cff
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_ClippedSourceRect method, IMSVidVideoRenderer.get_ClippedSourceRect, IMSVidVideoRenderer::get_ClippedSourceRect, IMSVidVideoRendererget_ClippedSourceRect, get_ClippedSourceRect, get_ClippedSourceRect method [Microsoft TV Technologies], get_ClippedSourceRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_clippedsourcerect, segment/IMSVidVideoRenderer::get_ClippedSourceRect
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
 - IMSVidVideoRenderer::get_ClippedSourceRect
 - segment/IMSVidVideoRenderer::get_ClippedSourceRect
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
 - IMSVidVideoRenderer.get_ClippedSourceRect
---

# IMSVidVideoRenderer::get_ClippedSourceRect


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ClippedSourceRect</b> method retrieves the clipping rectangle on the video source.

## -parameters

### -param pRect [out]

Receives an <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the current clipping mode is <b>sslClipByClipRect</b>, the VMR clips the video image to the video source rectangle, and stretches the clipped image to fill the Video Control's video window. For more information, see <a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_sourcesize">IMSVidVideoRenderer::put_SourceSize</a>.

The returned <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_clippedsourcerect">IMSVidVideoRenderer::put_ClippedSourceRect</a>