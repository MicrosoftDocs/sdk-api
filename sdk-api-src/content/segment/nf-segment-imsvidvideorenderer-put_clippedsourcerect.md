---
UID: NF:segment.IMSVidVideoRenderer.put_ClippedSourceRect
title: IMSVidVideoRenderer::put_ClippedSourceRect (segment.h)
description: The put_ClippedSourceRect method specifies the clipping rectangle on the video source.
helpviewer_keywords: ["IMSVidVideoRenderer interface [Microsoft TV Technologies]","put_ClippedSourceRect method","IMSVidVideoRenderer.put_ClippedSourceRect","IMSVidVideoRenderer::put_ClippedSourceRect","IMSVidVideoRendererput_ClippedSourceRect","mstv.imsvidvideorenderer_put_clippedsourcerect","put_ClippedSourceRect","put_ClippedSourceRect method [Microsoft TV Technologies]","put_ClippedSourceRect method [Microsoft TV Technologies]","IMSVidVideoRenderer interface","segment/IMSVidVideoRenderer::put_ClippedSourceRect"]
old-location: mstv\imsvidvideorenderer_put_clippedsourcerect.htm
tech.root: mstv
ms.assetid: c72d8134-ff6c-46b4-b567-35638aef53cd
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],put_ClippedSourceRect method, IMSVidVideoRenderer.put_ClippedSourceRect, IMSVidVideoRenderer::put_ClippedSourceRect, IMSVidVideoRendererput_ClippedSourceRect, mstv.imsvidvideorenderer_put_clippedsourcerect, put_ClippedSourceRect, put_ClippedSourceRect method [Microsoft TV Technologies], put_ClippedSourceRect method [Microsoft TV Technologies],IMSVidVideoRenderer interface, segment/IMSVidVideoRenderer::put_ClippedSourceRect
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
 - IMSVidVideoRenderer::put_ClippedSourceRect
 - segment/IMSVidVideoRenderer::put_ClippedSourceRect
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
 - IMSVidVideoRenderer.put_ClippedSourceRect
---

# IMSVidVideoRenderer::put_ClippedSourceRect


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_ClippedSourceRect</b> method specifies the clipping rectangle on the video source.

## -parameters

### -param pRect [in]

Pointer to an <a href="/previous-versions/windows/desktop/mstv/msvidrect">IMSVidRect</a> interface that specifies the rectangle.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

If the current clipping mode is <b>sslClipByClipRect</b>, the VMR clips the video image to the video source rectangle and stretches this to fill the Video Control's video window. For more information, see <a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-put_sourcesize">IMSVidVideoRenderer::put_SourceSize</a>.


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

<a href="/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidvideorenderer-get_clippedsourcerect">IMSVidVideoRenderer::get_ClippedSourceRect</a>