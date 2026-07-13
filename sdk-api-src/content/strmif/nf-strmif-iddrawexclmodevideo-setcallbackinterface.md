---
UID: NF:strmif.IDDrawExclModeVideo.SetCallbackInterface
title: IDDrawExclModeVideo::SetCallbackInterface (strmif.h)
description: The SetCallbackInterface method retrieves a pointer to the callback interface of the Overlay Mixer so that the calling application can be notified about adjustments to the display during video playback.
helpviewer_keywords: ["IDDrawExclModeVideo interface [DirectShow]","SetCallbackInterface method","IDDrawExclModeVideo.SetCallbackInterface","IDDrawExclModeVideo::SetCallbackInterface","IDDrawExclModeVideoSetCallbackInterface","SetCallbackInterface","SetCallbackInterface method [DirectShow]","SetCallbackInterface method [DirectShow]","IDDrawExclModeVideo interface","dshow.iddrawexclmodevideo_setcallbackinterface","strmif/IDDrawExclModeVideo::SetCallbackInterface"]
old-location: dshow\iddrawexclmodevideo_setcallbackinterface.htm
tech.root: dshow
ms.assetid: f8f885fe-d1a2-4635-9f30-d57ac0eb905e
ms.date: 4/26/2023
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetCallbackInterface method, IDDrawExclModeVideo.SetCallbackInterface, IDDrawExclModeVideo::SetCallbackInterface, IDDrawExclModeVideoSetCallbackInterface, SetCallbackInterface, SetCallbackInterface method [DirectShow], SetCallbackInterface method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setcallbackinterface, strmif/IDDrawExclModeVideo::SetCallbackInterface
req.header: strmif.h
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
 - IDDrawExclModeVideo::SetCallbackInterface
 - strmif/IDDrawExclModeVideo::SetCallbackInterface
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
 - IDDrawExclModeVideo.SetCallbackInterface
---

# IDDrawExclModeVideo::SetCallbackInterface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetCallbackInterface</code> method retrieves a pointer to the callback interface of the Overlay Mixer so that the calling application can be notified about adjustments to the display during video playback.

## -parameters

### -param pCallback [out]

Pointer to the object that implements the <a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideocallback">IDDrawExclModeVideoCallback</a> interface. If <i>pCallback</i> is <b>NULL</b>, the callback interface is set to <b>NULL</b> and no more callbacks are made. If there was a previous callback interface, it is released and no more callbacks are made to it. If <i>pCallback</i> is not <b>NULL</b> and this method returns S_OK, then the reference count of the object <i>pCallback</i> points to is incremented.

### -param dwFlags [in]

Must be zero.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
</table>

## -remarks

An application should use this method to get notification about the overlay size, position, or color key change happening, so that it can hide or show the video, or adjust the video at the start, end, or during playback. By calling this method, an application can access the <a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideocallback">IDDrawExclModeVideoCallback</a> interface and pass the pointer to that interface to the Overlay Mixer.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>