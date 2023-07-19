---
UID: NF:segment.IMSVidVideoRenderer.put__CustomCompositor
title: IMSVidVideoRenderer::put__CustomCompositor (segment.h)
description: The put__CustomCompositor method specifies a custom image compositor for the Video Mixing Renderer (VMR) to use.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put__CustomCompositor method","IMSVidVideoRenderer.put__CustomCompositor","IMSVidVideoRenderer::put__CustomCompositor","IMSVidVideoRendererput__CustomCompositor","mstv.imsvidvideorenderer_put__customcompositor","put__CustomCompositor","put__CustomCompositor method [Microsoft TV Technologies]","put__CustomCompositor method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put__CustomCompositor"]
old-location: mstv\imsvidvideorenderer_put__customcompositor.htm
tech.root: mstv
ms.assetid: ff99b253-20bc-4b8e-8624-ffcbb3b91857
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put__CustomCompositor method, IMSVidVideoRenderer.put__CustomCompositor, IMSVidVideoRenderer::put__CustomCompositor, IMSVidVideoRendererput__CustomCompositor, mstv.imsvidvideorenderer_put__customcompositor, put__CustomCompositor, put__CustomCompositor method [Microsoft TV Technologies], put__CustomCompositor method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put__CustomCompositor
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
 - IMSVidVideoRenderer::put__CustomCompositor
 - segment/IMSVidVideoRenderer::put__CustomCompositor
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
 - IMSVidVideoRenderer.put__CustomCompositor
---

# IMSVidVideoRenderer::put__CustomCompositor


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put__CustomCompositor</b> method specifies a custom image compositor for the Video Mixing Renderer (VMR) to use.

## -parameters

### -param Compositor [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagecompositor">IVMRImageCompositor</a> interface of the image compositor.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__customcompositor">IMSVidVideoRenderer::get__CustomCompositor</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositorclass">IMSVidVideoRenderer::put__CustomCompositorClass</a>