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

# IMSVidVideoRenderer::put_ClippedSourceRect


## -description


The <b>put_ClippedSourceRect</b> method specifies the clipping rectangle on the video source.


## -parameters




### -param pRect [in]

Pointer to an <a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect</a> interface that specifies the rectangle.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



If the current clipping mode is <b>sslClipByClipRect</b>, the VMR clips the video image to the video source rectangle and stretches this to fill the Video Control's video window. For more information, see <a href="https://msdn.microsoft.com/c792f064-a137-4872-8c79-6e924b6023f0">IMSVidVideoRenderer::put_SourceSize</a>.


#### Examples

The following example clips the video image to the upper left corner of the source rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
CComPtr&lt;IMSVidVideoRenderer&gt; pVideo;
HRESULT hr = pVideoControl-&gt;get_VideoRendererActive(&amp;pVideo);
if (SUCCEEDED(hr))
{
    long lWidth, lHeight;
    CComPtr&lt;IMSVidRect&gt; pRect;
    
    hr = pVideo-&gt;get_AvailableSourceRect(&amp;pRect);
    pRect-&gt;get_Height(&amp;lHeight);
    pRect-&gt;get_Width(&amp;lWidth);
    pRect-&gt;put_Height(lHeight / 2);
    pRect-&gt;put_Width(lWidth / 2);
    pVideo-&gt;put_SourceSize(sslClipByClipRect);
    hr = pVideo-&gt;put_ClippedSourceRect(pRect);
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/d40d39d9-41a4-42e1-b0d0-4a6299fd1cff">IMSVidVideoRenderer::get_ClippedSourceRect</a>
 

 

