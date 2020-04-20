---
UID: NF:segment.IMSVidVideoRenderer.put_CustomCompositorClass
title: IMSVidVideoRenderer::put_CustomCompositorClass (segment.h)
description: The put_CustomCompositorClass method specifies the class identifier (CLSID) of a custom image compositor, as a BSTR.helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_CustomCompositorClass method","IMSVidVideoRenderer.put_CustomCompositorClass","IMSVidVideoRenderer::put_CustomCompositorClass","IMSVidVideoRendererput_CustomCompositorClass","mstv.imsvidvideorenderer_put_customcompositorclass","put_CustomCompositorClass","put_CustomCompositorClass method [Microsoft TV Technologies]","put_CustomCompositorClass method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_CustomCompositorClass"]
old-location: mstv\imsvidvideorenderer_put_customcompositorclass.htm
tech.root: mstv
ms.assetid: 399a5151-b26a-4c33-9dd9-e7abb23cbd1c
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_CustomCompositorClass method, IMSVidVideoRenderer.put_CustomCompositorClass, IMSVidVideoRenderer::put_CustomCompositorClass, IMSVidVideoRendererput_CustomCompositorClass, mstv.imsvidvideorenderer_put_customcompositorclass, put_CustomCompositorClass, put_CustomCompositorClass method [Microsoft TV Technologies], put_CustomCompositorClass method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_CustomCompositorClass
f1_keywords:
- segment/IMSVidVideoRenderer.put_CustomCompositorClass
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidVideoRenderer.put_CustomCompositorClass
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer::put_CustomCompositorClass


## -description


The <b>put_CustomCompositorClass</b> method specifies the class identifier (CLSID) of a custom image compositor, as a <b>BSTR</b>.


## -parameters




### -param CompositorCLSID [in]

Specifies the CLSID as a string.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This method is provided for Automation clients. C++ applications can use the <a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put__customcompositorclass">IMSVidVideoRenderer::put__CustomCompositorClass</a> method, which specifies a <b>GUID</b> rather than a <b>BSTR</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_customcompositorclass">IMSVidVideoRenderer::get_CustomCompositorClass</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

