---
UID: NF:strmif.IAMStreamSelect.Count
title: IAMStreamSelect::Count (strmif.h)
description: The Count method retrieves the number of available streams.
helpviewer_keywords: ["Count","Count method [DirectShow]","Count method [DirectShow]","IAMStreamSelect interface","IAMStreamSelect interface [DirectShow]","Count method","IAMStreamSelect.Count","IAMStreamSelect::Count","IAMStreamSelectCount","dshow.iamstreamselect_count","strmif/IAMStreamSelect::Count"]
old-location: dshow\iamstreamselect_count.htm
tech.root: dshow
ms.assetid: 5104ce98-5b13-409a-9226-0c089ee8bb1e
ms.date: 4/26/2023
ms.keywords: Count, Count method [DirectShow], Count method [DirectShow],IAMStreamSelect interface, IAMStreamSelect interface [DirectShow],Count method, IAMStreamSelect.Count, IAMStreamSelect::Count, IAMStreamSelectCount, dshow.iamstreamselect_count, strmif/IAMStreamSelect::Count
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
 - IAMStreamSelect::Count
 - strmif/IAMStreamSelect::Count
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
 - IAMStreamSelect.Count
---

# IAMStreamSelect::Count


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Count</code> method retrieves the number of available streams.

## -parameters

### -param pcStreams [out]

Receives the number of streams.

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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pins are not connected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamstreamselect">IAMStreamSelect Interface</a>