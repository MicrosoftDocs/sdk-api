---
UID: NF:amvideo.IFullScreenVideoEx.IsModeEnabled
title: IFullScreenVideoEx::IsModeEnabled (amvideo.h)
description: The IsModeEnabled method queries whether a specified display mode is enabled.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","IsModeEnabled method","IFullScreenVideoEx.IsModeEnabled","IFullScreenVideoEx::IsModeEnabled","IFullScreenVideoIsModeEnabled","IsModeEnabled","IsModeEnabled method [DirectShow]","IsModeEnabled method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::IsModeEnabled","dshow.ifullscreenvideoex_ismodeenabled"]
old-location: dshow\ifullscreenvideoex_ismodeenabled.htm
tech.root: dshow
ms.assetid: 97d8b9f8-4dbf-4b49-b32f-4513c9e5186e
ms.date: 4/26/2023
ms.keywords: IFullScreenVideoEx interface [DirectShow],IsModeEnabled method, IFullScreenVideoEx.IsModeEnabled, IFullScreenVideoEx::IsModeEnabled, IFullScreenVideoIsModeEnabled, IsModeEnabled, IsModeEnabled method [DirectShow], IsModeEnabled method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::IsModeEnabled, dshow.ifullscreenvideoex_ismodeenabled
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
 - IFullScreenVideoEx::IsModeEnabled
 - amvideo/IFullScreenVideoEx::IsModeEnabled
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
 - IFullScreenVideoEx.IsModeEnabled
---

# IFullScreenVideoEx::IsModeEnabled


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsModeEnabled</code> method queries whether a specified display mode is enabled.

## -parameters

### -param Mode [in]

Index of the display mode to query.

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
The display mode is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The display mode is enabled.

</td>
</tr>
</table>

## -remarks

The Full Screen Renderer supports a static set of display modes. By default, every mode is enabled. You can enable or disable a display mode by calling the <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-setenabled">IFullScreenVideoEx::SetEnabled</a>. The <b>IsEnabled</b> method retrieves the current setting for the specified mode.

The video card on the user's system might not support every mode. The Full Screen Renderer will not use a mode that the video card does not support, even if that mode is enabled. To determine whether the card supports a particular mode, call the <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable">IFullScreenVideoEx::IsModeAvailable</a> method. If a mode is disabled, the Full Screen Renderer will not use it, even if the card supports it.

Display modes are indexed from zero. The <a href="/windows/desktop/api/amvideo/nf-amvideo-ifullscreenvideoex-countmodes">IFullScreenVideoEx::CountModes</a> method returns the number of modes.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>