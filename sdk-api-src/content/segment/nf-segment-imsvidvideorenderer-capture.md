---
UID: NF:segment.IMSVidVideoRenderer.Capture
title: IMSVidVideoRenderer::Capture
author: windows-driver-content
description: The Capture method captures the video frame that is currently being rendered by the Video Mixing Renderer (VMR).
old-location: mstv\imsvidvideorenderer_capture.htm
old-project: mstv
ms.assetid: 05287e53-a988-43cc-ac41-5024a217621a
ms.author: windowsdriverdev
ms.date: 5/8/2018
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRenderer.Capture
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidVideoRenderer::Capture


## -description


The <b>Capture</b> method captures the video frame that is currently being rendered by the Video Mixing Renderer (VMR).


## -parameters




### -param currentImage






#### - ppcurrentImage [out]

Receives an <b>IPictureDisp</b> interface pointer.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The returned <b>IPictureDisp</b> interface has an outstanding reference count. The caller must release the interface.

For information about the <b>IPictureDisp</b> interface, see the Microsoft Platform SDK documentation.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComPtr&lt;IMSVidCtl&gt; m_pVideoControl; // Pointer to the Video Control.

/* Build and run the filter graph (not shown). */

// Find the video renderer
CComPtr&lt;IMSVidVideoRenderer&gt; pVideo;
hr = m_pVideoControl-&gt;get_VideoRendererActive(&amp;pVideo);
if (SUCCEEDED(hr))
{
    // Capture the image.
    CComPtr&lt;IPictureDisp&gt; pPic;
    hr = pVideo-&gt;Capture(&amp;pPic);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

