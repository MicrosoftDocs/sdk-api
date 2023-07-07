---
UID: NF:segment.IMSVidVideoRenderer.put__CustomCompositorClass
title: IMSVidVideoRenderer::put__CustomCompositorClass (segment.h)
description: The put__CustomCompositorClass method specifies the class identifier (CLSID) of a custom image compositor, as a GUID.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put__CustomCompositorClass method","IMSVidVideoRenderer.put__CustomCompositorClass","IMSVidVideoRenderer::put__CustomCompositorClass","IMSVidVideoRendererput__CustomCompositorClass","mstv.imsvidvideorenderer_put__customcompositorclass","put__CustomCompositorClass","put__CustomCompositorClass method [Microsoft TV Technologies]","put__CustomCompositorClass method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put__CustomCompositorClass"]
old-location: mstv\imsvidvideorenderer_put__customcompositorclass.htm
tech.root: mstv
ms.assetid: 031af4a5-6eed-44c9-9b0c-f472d709db66
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put__CustomCompositorClass method, IMSVidVideoRenderer.put__CustomCompositorClass, IMSVidVideoRenderer::put__CustomCompositorClass, IMSVidVideoRendererput__CustomCompositorClass, mstv.imsvidvideorenderer_put__customcompositorclass, put__CustomCompositorClass, put__CustomCompositorClass method [Microsoft TV Technologies], put__CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put__CustomCompositorClass
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
 - IMSVidVideoRenderer::put__CustomCompositorClass
 - segment/IMSVidVideoRenderer::put__CustomCompositorClass
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
 - IMSVidVideoRenderer.put__CustomCompositorClass
---

# IMSVidVideoRenderer::put__CustomCompositorClass


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put__CustomCompositorClass</b> method specifies the class identifier (CLSID) of a custom image compositor, as a <b>GUID</b>.

## -parameters

### -param CompositorCLSID [in]

Specifies the CLSID of the custom compositor.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

Applications can provide their own compositors to perform custom image compositing. For more information, see <a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__customcompositorclass">IMSVidVideoRenderer::get__CustomCompositorClass</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositor">IMSVidVideoRenderer::put__CustomCompositor</a>