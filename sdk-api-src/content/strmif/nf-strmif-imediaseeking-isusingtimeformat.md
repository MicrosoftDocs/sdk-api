---
UID: NF:strmif.IMediaSeeking.IsUsingTimeFormat
title: IMediaSeeking::IsUsingTimeFormat (strmif.h)
description: The IsUsingTimeFormat method determines whether seek operations are currently using a specified time format.
helpviewer_keywords: ["IMediaSeeking interface [DirectShow]","IsUsingTimeFormat method","IMediaSeeking.IsUsingTimeFormat","IMediaSeeking::IsUsingTimeFormat","IMediaSeekingIsUsingTimeFormat","IsUsingTimeFormat","IsUsingTimeFormat method [DirectShow]","IsUsingTimeFormat method [DirectShow]","IMediaSeeking interface","dshow.imediaseeking_isusingtimeformat","strmif/IMediaSeeking::IsUsingTimeFormat"]
old-location: dshow\imediaseeking_isusingtimeformat.htm
tech.root: dshow
ms.assetid: 27211946-9b05-40fc-823e-efad87a730a3
ms.date: 4/26/2023
ms.keywords: IMediaSeeking interface [DirectShow],IsUsingTimeFormat method, IMediaSeeking.IsUsingTimeFormat, IMediaSeeking::IsUsingTimeFormat, IMediaSeekingIsUsingTimeFormat, IsUsingTimeFormat, IsUsingTimeFormat method [DirectShow], IsUsingTimeFormat method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_isusingtimeformat, strmif/IMediaSeeking::IsUsingTimeFormat
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
 - IMediaSeeking::IsUsingTimeFormat
 - strmif/IMediaSeeking::IsUsingTimeFormat
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
 - IMediaSeeking.IsUsingTimeFormat
---

# IMediaSeeking::IsUsingTimeFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IsUsingTimeFormat</code> method determines whether seek operations are currently using a specified time format.

## -parameters

### -param pFormat [in]

Pointer to a GUID that specifies the time format. See <a href="/windows/desktop/DirectShow/time-format-guids">Time Format GUIDs</a>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified format is not the current format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The specified format is the current format.

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

## -remarks

This method is slightly more efficient than the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-gettimeformat">IMediaSeeking::GetTimeFormat</a> method, because it does not require copying the GUID.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a>