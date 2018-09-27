---
UID: NF:segment.IMSVidVideoRenderer.Capture
title: IMSVidVideoRenderer::Capture
author: windows-sdk-content
description: The Capture method captures the video frame that is currently being rendered by the Video Mixing Renderer (VMR).
old-location: mstv\imsvidvideorenderer_capture.htm
tech.root: MSTV
ms.assetid: 05287e53-a988-43cc-ac41-5024a217621a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Capture, Capture method [Microsoft TV Technologies], Capture method [Microsoft TV Technologies],IMSVidVideoRenderer interface, IMSVidVideoRenderer interface [Microsoft TV Technologies],Capture method, IMSVidVideoRenderer.Capture, IMSVidVideoRenderer::Capture, IMSVidVideoRendererCapture, mstv.imsvidvideorenderer_capture, segment/IMSVidVideoRenderer::Capture
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IMSVidVideoRenderer.Capture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::Capture


## -description


The <b>Capture</b> method captures the video frame that is currently being rendered by the Video Mixing Renderer (VMR).


## -parameters




### -param currentImage

TBD




#### - ppcurrentImage [out]

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




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

