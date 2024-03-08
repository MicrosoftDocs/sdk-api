---
UID: NF:segment.IMSVidVideoRenderer.put_CustomCompositorClass
title: IMSVidVideoRenderer::put_CustomCompositorClass (segment.h)
description: The put_CustomCompositorClass method specifies the class identifier (CLSID) of a custom image compositor, as a BSTR.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_CustomCompositorClass method","IMSVidVideoRenderer.put_CustomCompositorClass","IMSVidVideoRenderer::put_CustomCompositorClass","IMSVidVideoRendererput_CustomCompositorClass","mstv.imsvidvideorenderer_put_customcompositorclass","put_CustomCompositorClass","put_CustomCompositorClass method [Microsoft TV Technologies]","put_CustomCompositorClass method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_CustomCompositorClass"]
old-location: mstv\imsvidvideorenderer_put_customcompositorclass.htm
tech.root: mstv
ms.assetid: 399a5151-b26a-4c33-9dd9-e7abb23cbd1c
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_CustomCompositorClass method, IMSVidVideoRenderer.put_CustomCompositorClass, IMSVidVideoRenderer::put_CustomCompositorClass, IMSVidVideoRendererput_CustomCompositorClass, mstv.imsvidvideorenderer_put_customcompositorclass, put_CustomCompositorClass, put_CustomCompositorClass method [Microsoft TV Technologies], put_CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_CustomCompositorClass
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
 - IMSVidVideoRenderer::put_CustomCompositorClass
 - segment/IMSVidVideoRenderer::put_CustomCompositorClass
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
 - IMSVidVideoRenderer.put_CustomCompositorClass
---

# IMSVidVideoRenderer::put_CustomCompositorClass


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_CustomCompositorClass</b> method specifies the class identifier (CLSID) of a custom image compositor, as a <b>BSTR</b>.

## -parameters

### -param CompositorCLSID [in]

Specifies the CLSID as a string.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method is provided for Automation clients. C++ applications can use the <a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositorclass">IMSVidVideoRenderer::put__CustomCompositorClass</a> method, which specifies a <b>GUID</b> rather than a <b>BSTR</b>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_customcompositorclass">IMSVidVideoRenderer::get_CustomCompositorClass</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>