---
UID: NF:amvideo.IFullScreenVideoEx.SetClipFactor
title: IFullScreenVideoEx::SetClipFactor (amvideo.h)
description: The SetClipFactor method specifies the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetClipFactor method","IFullScreenVideoEx.SetClipFactor","IFullScreenVideoEx::SetClipFactor","IFullScreenVideoSetClipFactor","SetClipFactor","SetClipFactor method [DirectShow]","SetClipFactor method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetClipFactor","dshow.ifullscreenvideoex_setclipfactor"]
old-location: dshow\ifullscreenvideoex_setclipfactor.htm
tech.root: dshow
ms.assetid: 3e2cefd3-491f-4ba4-a234-047fe4e6c6cc
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetClipFactor method, IFullScreenVideoEx.SetClipFactor, IFullScreenVideoEx::SetClipFactor, IFullScreenVideoSetClipFactor, SetClipFactor, SetClipFactor method [DirectShow], SetClipFactor method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetClipFactor, dshow.ifullscreenvideoex_setclipfactor
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFullScreenVideoEx::SetClipFactor
 - amvideo/IFullScreenVideoEx::SetClipFactor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx.SetClipFactor
---

# IFullScreenVideoEx::SetClipFactor


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetClipFactor</code> method specifies the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip.



For example, suppose the display mode is 320 x 200 and the video is 352 x 288 pixels. Assuming the decoder cannot shrink the video, the display will clip about 25 percent of the image. The clip factor specifies the upper range that is permitted. The default value is 25%.

## -parameters

### -param ClipFactor [in]

Specifies the maximum allowable amount of the image to clip. The value is expressed as a percentage from 0 to 100.

## -returns

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>