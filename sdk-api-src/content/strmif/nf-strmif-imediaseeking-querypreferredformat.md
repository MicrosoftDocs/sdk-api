---
UID: NF:strmif.IMediaSeeking.QueryPreferredFormat
title: IMediaSeeking::QueryPreferredFormat (strmif.h)
description: The QueryPreferredFormat method retrieves the preferred time format for seeking.
helpviewer_keywords: ["IMediaSeeking interface [DirectShow]","QueryPreferredFormat method","IMediaSeeking.QueryPreferredFormat","IMediaSeeking::QueryPreferredFormat","IMediaSeekingQueryPreferredFormat","QueryPreferredFormat","QueryPreferredFormat method [DirectShow]","QueryPreferredFormat method [DirectShow]","IMediaSeeking interface","dshow.imediaseeking_querypreferredformat","strmif/IMediaSeeking::QueryPreferredFormat"]
old-location: dshow\imediaseeking_querypreferredformat.htm
tech.root: dshow
ms.assetid: 16fd71d6-c162-493c-9bca-479d59da5031
ms.date: 4/26/2023
ms.keywords: IMediaSeeking interface [DirectShow],QueryPreferredFormat method, IMediaSeeking.QueryPreferredFormat, IMediaSeeking::QueryPreferredFormat, IMediaSeekingQueryPreferredFormat, QueryPreferredFormat, QueryPreferredFormat method [DirectShow], QueryPreferredFormat method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_querypreferredformat, strmif/IMediaSeeking::QueryPreferredFormat
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
 - IMediaSeeking::QueryPreferredFormat
 - strmif/IMediaSeeking::QueryPreferredFormat
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
 - IMediaSeeking.QueryPreferredFormat
---

# IMediaSeeking::QueryPreferredFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>QueryPreferredFormat</code> method retrieves the preferred time format for seeking.

## -parameters

### -param pFormat [out]

Pointer to a variable that receives a GUID specifying the time format. See <a href="/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a>