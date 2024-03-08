---
UID: NF:segment.IMSVidVideoRenderer.Capture
title: IMSVidVideoRenderer::Capture (segment.h)
description: The Capture method captures the video frame that is currently being rendered by the Video Mixing Renderer (VMR).
helpviewer_keywords: ["Capture","Capture method [Microsoft TV Technologies]","Capture method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","IMSVidVideoRenderer interface [Microsoft TV Technologies]","Capture method","IMSVidVideoRenderer.Capture","IMSVidVideoRenderer::Capture","IMSVidVideoRendererCapture","mstv.imsvidvideorenderer_capture","segment/IMSVidVideoRenderer::Capture"]
old-location: mstv\imsvidvideorenderer_capture.htm
tech.root: mstv
ms.assetid: 05287e53-a988-43cc-ac41-5024a217621a
ms.date: 12/05/2018
ms.keywords: Capture, Capture method [Microsoft TV Technologies], Capture method [Microsoft TV Technologies],IMSVidVideoRenderer interface, IMSVidVideoRenderer interface [Microsoft TV Technologies],Capture method, IMSVidVideoRenderer.Capture, IMSVidVideoRenderer::Capture, IMSVidVideoRendererCapture, mstv.imsvidvideorenderer_capture, segment/IMSVidVideoRenderer::Capture
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
 - IMSVidVideoRenderer::Capture
 - segment/IMSVidVideoRenderer::Capture
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
 - IMSVidVideoRenderer.Capture
---

# IMSVidVideoRenderer::Capture


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Capture</b> method captures the video frame that is currently being rendered by the Video Mixing Renderer (VMR).

## -parameters

### -param currentImage [out]

Receives an <b>IPictureDisp</b> interface pointer.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The returned <b>IPictureDisp</b> interface has an outstanding reference count. The caller must release the interface.

For information about the <b>IPictureDisp</b> interface, see the Microsoft Platform SDK documentation.


#### Examples


```cpp

CComPtr<IMSVidCtl> m_pVideoControl; // Pointer to the Video Control.

/* Build and run the filter graph (not shown). */

// Find the video renderer
CComPtr<IMSVidVideoRenderer> pVideo;
hr = m_pVideoControl->get_VideoRendererActive(&pVideo);
if (SUCCEEDED(hr))
{
    // Capture the image.
    CComPtr<IPictureDisp> pPic;
    hr = pVideo->Capture(&pPic);
}

```

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>