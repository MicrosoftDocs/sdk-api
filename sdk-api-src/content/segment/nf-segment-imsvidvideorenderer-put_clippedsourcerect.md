---
UID: NF:segment.IMSVidVideoRenderer.put_ClippedSourceRect
title: IMSVidVideoRenderer::put_ClippedSourceRect method
author: windows-driver-content
description: The put_ClippedSourceRect method specifies the clipping rectangle on the video source.
old-location: mstv\imsvidvideorenderer_put_clippedsourcerect.htm
old-project: mstv
ms.assetid: c72d8134-ff6c-46b4-b567-35638aef53cd
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IMSVidVideoRenderer, IMSVidVideoRenderer interface [Microsoft TV Technologies], put_ClippedSourceRect method, IMSVidVideoRenderer::put_ClippedSourceRect, IMSVidVideoRendererput_ClippedSourceRect, mstv.imsvidvideorenderer_put_clippedsourcerect, put_ClippedSourceRect method [Microsoft TV Technologies], put_ClippedSourceRect method [Microsoft TV Technologies], IMSVidVideoRenderer interface, put_ClippedSourceRect,IMSVidVideoRenderer.put_ClippedSourceRect, segment/IMSVidVideoRenderer::put_ClippedSourceRect
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
-	IMSVidVideoRenderer.put_ClippedSourceRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMSVidVideoRenderer::put_ClippedSourceRect method


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
 

 

