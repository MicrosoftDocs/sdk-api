---
UID: NF:amvideo.IFullScreenVideoEx.GetCaption
title: IFullScreenVideoEx::GetCaption (amvideo.h)
description: The GetCaption method retrieves the caption associated with the full-screen window.
helpviewer_keywords: ["GetCaption","GetCaption method [DirectShow]","GetCaption method [DirectShow]","IFullScreenVideoEx interface","IFullScreenVideoEx interface [DirectShow]","GetCaption method","IFullScreenVideoEx.GetCaption","IFullScreenVideoEx::GetCaption","IFullScreenVideoGetCaption","amvideo/IFullScreenVideoEx::GetCaption","dshow.ifullscreenvideoex_getcaption"]
old-location: dshow\ifullscreenvideoex_getcaption.htm
tech.root: dshow
ms.assetid: 0757da34-cfc5-4a40-9ad0-03bd016ad828
ms.date: 4/26/2023
ms.keywords: GetCaption, GetCaption method [DirectShow], GetCaption method [DirectShow],IFullScreenVideoEx interface, IFullScreenVideoEx interface [DirectShow],GetCaption method, IFullScreenVideoEx.GetCaption, IFullScreenVideoEx::GetCaption, IFullScreenVideoGetCaption, amvideo/IFullScreenVideoEx::GetCaption, dshow.ifullscreenvideoex_getcaption
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
 - IFullScreenVideoEx::GetCaption
 - amvideo/IFullScreenVideoEx::GetCaption
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
 - IFullScreenVideoEx.GetCaption
---

# IFullScreenVideoEx::GetCaption


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetCaption</code> method retrieves the caption associated with the full-screen window.

## -parameters

### -param pstrCaption [out]

Pointer to a <b>BSTR</b> that receives the caption.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

The caption is visible when the window is minimized.

The caller must release the returned string, by calling the <b>SysFreeString</b> function.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>