---
UID: NF:segment.IMSVidVideoRenderer.get__CustomCompositor
title: IMSVidVideoRenderer::get__CustomCompositor (segment.h)
description: The get__CustomCompositor method retrieves the Video Mixing Renderer's current image compositor.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get__CustomCompositor method","IMSVidVideoRenderer.get__CustomCompositor","IMSVidVideoRenderer::get__CustomCompositor","IMSVidVideoRendererget__CustomCompositor","get__CustomCompositor","get__CustomCompositor method [Microsoft TV Technologies]","get__CustomCompositor method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get__customcompositor","segment/IMSVidVideoRenderer::get__CustomCompositor"]
old-location: mstv\imsvidvideorenderer_get__customcompositor.htm
tech.root: mstv
ms.assetid: cafdc512-2994-4374-9396-b0bb946bc490
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get__CustomCompositor method, IMSVidVideoRenderer.get__CustomCompositor, IMSVidVideoRenderer::get__CustomCompositor, IMSVidVideoRendererget__CustomCompositor, get__CustomCompositor, get__CustomCompositor method [Microsoft TV Technologies], get__CustomCompositor method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get__customcompositor, segment/IMSVidVideoRenderer::get__CustomCompositor
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
 - IMSVidVideoRenderer::get__CustomCompositor
 - segment/IMSVidVideoRenderer::get__CustomCompositor
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
 - IMSVidVideoRenderer.get__CustomCompositor
---

# IMSVidVideoRenderer::get__CustomCompositor


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get__CustomCompositor</b> method retrieves the Video Mixing Renderer's current image compositor.

## -parameters

### -param Compositor [out]

Receives an <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor</a> interface pointer .

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>.

The returned <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor</a> interface has an outstanding reference count. The caller must release the interface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__customcompositorclass">IMSVidVideoRenderer::get__CustomCompositorClass</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositor">IMSVidVideoRenderer::put__CustomCompositor</a>