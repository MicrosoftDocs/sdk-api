---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

