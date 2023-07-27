---
UID: NF:strmif.IDDrawExclModeVideoCallback.OnUpdateColorKey
title: IDDrawExclModeVideoCallback::OnUpdateColorKey (strmif.h)
description: The OnUpdateColorKey method informs the application that the color key has changed so that the application can use the new color key to overlay graphics on the video.
helpviewer_keywords: ["IDDrawExclModeVideoCallback interface [DirectShow]","OnUpdateColorKey method","IDDrawExclModeVideoCallback.OnUpdateColorKey","IDDrawExclModeVideoCallback::OnUpdateColorKey","IDDrawExclModeVideoCallbackOnUpdateColorKey","OnUpdateColorKey","OnUpdateColorKey method [DirectShow]","OnUpdateColorKey method [DirectShow]","IDDrawExclModeVideoCallback interface","dshow.iddrawexclmodevideocallback_onupdatecolorkey","strmif/IDDrawExclModeVideoCallback::OnUpdateColorKey"]
old-location: dshow\iddrawexclmodevideocallback_onupdatecolorkey.htm
tech.root: dshow
ms.assetid: 87d4a4b5-f67e-46f6-956a-1c9c309bfde7
ms.date: 4/26/2023
ms.keywords: IDDrawExclModeVideoCallback interface [DirectShow],OnUpdateColorKey method, IDDrawExclModeVideoCallback.OnUpdateColorKey, IDDrawExclModeVideoCallback::OnUpdateColorKey, IDDrawExclModeVideoCallbackOnUpdateColorKey, OnUpdateColorKey, OnUpdateColorKey method [DirectShow], OnUpdateColorKey method [DirectShow],IDDrawExclModeVideoCallback interface, dshow.iddrawexclmodevideocallback_onupdatecolorkey, strmif/IDDrawExclModeVideoCallback::OnUpdateColorKey
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
 - IDDrawExclModeVideoCallback::OnUpdateColorKey
 - strmif/IDDrawExclModeVideoCallback::OnUpdateColorKey
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
 - IDDrawExclModeVideoCallback.OnUpdateColorKey
---

# IDDrawExclModeVideoCallback::OnUpdateColorKey


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>OnUpdateColorKey</code> method informs the application that the color key has changed so that the application can use the new color key to overlay graphics on the video.

## -parameters

### -param pKey [out]

Pointer to a [COLORKEY](/windows/desktop/api/strmif/ns-strmif-colorkey) structure that contains the key type and a palette index.

### -param dwColor [out]

Value indicating the 8-bit palette index of the <b>COLORKEY</b> returned in <i>pKey</i>, if the current display mode is 8-bit palettized. Otherwise, it is a value representing the color key in the pixel format of the current display mode.

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
One of the parameters is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideocallback">IDDrawExclModeVideoCallback Interface</a>