---
UID: NF:segment.IMSVidVideoRenderer.get_CustomCompositorClass
title: IMSVidVideoRenderer::get_CustomCompositorClass (segment.h)
description: The get_CustomCompositorClass method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a BSTR.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","get_CustomCompositorClass method","IMSVidVideoRenderer.get_CustomCompositorClass","IMSVidVideoRenderer::get_CustomCompositorClass","IMSVidVideoRendererget_CustomCompositorClass","get_CustomCompositorClass","get_CustomCompositorClass method [Microsoft TV Technologies]","get_CustomCompositorClass method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","mstv.imsvidvideorenderer_get_customcompositorclass","segment/IMSVidVideoRenderer::get_CustomCompositorClass"]
old-location: mstv\imsvidvideorenderer_get_customcompositorclass.htm
tech.root: mstv
ms.assetid: d6ff1968-e891-432d-9271-f6d6a6a8a756
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_CustomCompositorClass method, IMSVidVideoRenderer.get_CustomCompositorClass, IMSVidVideoRenderer::get_CustomCompositorClass, IMSVidVideoRendererget_CustomCompositorClass, get_CustomCompositorClass, get_CustomCompositorClass method [Microsoft TV Technologies], get_CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_customcompositorclass, segment/IMSVidVideoRenderer::get_CustomCompositorClass
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
 - IMSVidVideoRenderer::get_CustomCompositorClass
 - segment/IMSVidVideoRenderer::get_CustomCompositorClass
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
 - IMSVidVideoRenderer.get_CustomCompositorClass
---

# IMSVidVideoRenderer::get_CustomCompositorClass


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_CustomCompositorClass</b> method retrieves the class identifier (CLSID) of the Video Mixing Renderer's current image compositor, as a <b>BSTR</b>.

## -parameters

### -param CompositorCLSID [out]

Receives a string representation of the CLSID.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

This method is provided for Automation clients. C++ applications can use the <a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get__customcompositorclass">IMSVidVideoRenderer::get__CustomCompositorClass</a> method, which returns a <b>GUID</b> rather than a <b>BSTR</b>.

The caller must free the returned string, using the <b>SysFreeString</b> function.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_customcompositorclass">IMSVidVideoRenderer::put_CustomCompositorClass</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>