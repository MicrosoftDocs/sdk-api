---
UID: NF:segment.IMSVidVideoRenderer.put_ClippedSourceRect
title: IMSVidVideoRenderer::put_ClippedSourceRect (segment.h)
author: windows-sdk-content
description: The put_ClippedSourceRect method specifies the clipping rectangle on the video source.
old-location: mstv\imsvidvideorenderer_put_clippedsourcerect.htm
tech.root: mstv
ms.assetid: c72d8134-ff6c-46b4-b567-35638aef53cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_ClippedSourceRect method, IMSVidVideoRenderer.put_ClippedSourceRect, IMSVidVideoRenderer::put_ClippedSourceRect, IMSVidVideoRendererput_ClippedSourceRect, mstv.imsvidvideorenderer_put_clippedsourcerect, put_ClippedSourceRect, put_ClippedSourceRect method [Microsoft TV Technologies], put_ClippedSourceRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_ClippedSourceRect
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
 - IMSVidVideoRenderer.put_ClippedSourceRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If the current clipping mode is <b>sslClipByClipRect</b>, the VMR clips the video image to the video source rectangle and stretches this to fill the Video Control's video window. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Dd694755(v=VS.85).aspx">IMSVidVideoRenderer::put_SourceSize</a>.


#### Examples

The following example clips the video image to the upper left corner of the source rectangle.


```cpp

CComPtr<IMSVidVideoRenderer> pVideo;
HRESULT hr = pVideoControl->get_VideoRendererActive(&pVideo);
if (SUCCEEDED(hr))
{
    long lWidth, lHeight;
    CComPtr<IMSVidRect> pRect;
    
    hr = pVideo->get_AvailableSourceRect(&pRect);
    pRect->get_Height(&lHeight);
    pRect->get_Width(&lWidth);
    pRect->put_Height(lHeight / 2);
    pRect->put_Width(lWidth / 2);
    pVideo->put_SourceSize(sslClipByClipRect);
    hr = pVideo->put_ClippedSourceRect(pRect);
}


```





## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694733(v=VS.85).aspx">IMSVidVideoRenderer::get_ClippedSourceRect</a>
 

 

