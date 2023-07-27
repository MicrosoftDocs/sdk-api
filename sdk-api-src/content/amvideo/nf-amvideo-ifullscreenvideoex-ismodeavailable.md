---
UID: NF:amvideo.IFullScreenVideoEx.IsModeAvailable
title: IFullScreenVideoEx::IsModeAvailable (amvideo.h)
description: The IsModeAvailable method queries whether a specified display mode is available.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","IsModeAvailable method","IFullScreenVideoEx.IsModeAvailable","IFullScreenVideoEx::IsModeAvailable","IFullScreenVideoIsModeAvailable","IsModeAvailable","IsModeAvailable method [DirectShow]","IsModeAvailable method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::IsModeAvailable","dshow.ifullscreenvideoex_ismodeavailable"]
old-location: dshow\ifullscreenvideoex_ismodeavailable.htm
tech.root: dshow
ms.assetid: 9b05d6c6-522c-46b8-90b5-c4650cee5f6b
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsModeAvailable method, IFullScreenVideoEx.IsModeAvailable, IFullScreenVideoEx::IsModeAvailable, IFullScreenVideoIsModeAvailable, IsModeAvailable, IsModeAvailable method [DirectShow], IsModeAvailable method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsModeAvailable, dshow.ifullscreenvideoex_ismodeavailable
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
 - IFullScreenVideoEx::IsModeAvailable
 - amvideo/IFullScreenVideoEx::IsModeAvailable
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
 - IFullScreenVideoEx.IsModeAvailable
---

# IFullScreenVideoEx::IsModeAvailable


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsModeAvailable</code> method queries whether a specified display mode is available.

## -parameters

### -param Mode [in]

Index of the display mode.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The display mode is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The display mode is available.

</td>
</tr>
</table>

## -remarks

The Full Screen Renderer supports a static set of display modes. However, the video card on the user's system might not support every mode. If a particular display mode is not supported by the video card, this method returns S_FALSE. Even if a particular mode is available, it will not necessarily be used for video playback. The mode must also be compatible with the filters in the filter graph.

You can disable a display mode by calling the <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setenabled">IFullScreenVideoEx::SetEnabled</a> method. The Full Screen Renderer will not use a disabled mode, even if the video card supports it.

Display modes are indexed from zero. The <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-countmodes">IFullScreenVideoEx::CountModes</a> method returns the number of modes.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>