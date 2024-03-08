---
UID: NF:strmif.IMediaSeeking.SetTimeFormat
title: IMediaSeeking::SetTimeFormat (strmif.h)
description: The SetTimeFormat method sets the time format for subsequent seek operations.
helpviewer_keywords: ["IMediaSeeking interface [DirectShow]","SetTimeFormat method","IMediaSeeking.SetTimeFormat","IMediaSeeking::SetTimeFormat","IMediaSeekingSetTimeFormat","SetTimeFormat","SetTimeFormat method [DirectShow]","SetTimeFormat method [DirectShow]","IMediaSeeking interface","dshow.imediaseeking_settimeformat","strmif/IMediaSeeking::SetTimeFormat"]
old-location: dshow\imediaseeking_settimeformat.htm
tech.root: dshow
ms.assetid: b6f64f8a-67b8-4297-8f0d-389001fa1681
ms.date: 4/26/2023
ms.keywords: IMediaSeeking interface [DirectShow],SetTimeFormat method, IMediaSeeking.SetTimeFormat, IMediaSeeking::SetTimeFormat, IMediaSeekingSetTimeFormat, SetTimeFormat, SetTimeFormat method [DirectShow], SetTimeFormat method [DirectShow],IMediaSeeking interface, dshow.imediaseeking_settimeformat, strmif/IMediaSeeking::SetTimeFormat
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
 - IMediaSeeking::SetTimeFormat
 - strmif/IMediaSeeking::SetTimeFormat
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
 - IMediaSeeking.SetTimeFormat
---

# IMediaSeeking::SetTimeFormat


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetTimeFormat</code> method sets the time format for subsequent seek operations.

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
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_WRONG_STATE</b></dt>
</dl>
</td>
<td width="60%">
Filter graph is not stopped.

</td>
</tr>
</table>

## -remarks

This method specifies the time units used by other <b>IMediaSeeking</b> methods, such as <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-getpositions">IMediaSeeking::GetPositions</a> and <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-setpositions">IMediaSeeking::SetPositions</a>. Whenever you call one of these other methods, any parameters that express time values are given in units of the current time format.

The default time format is <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> units (100 nanoseconds). Other time formats include frames, samples, and bytes. To determine if a given format is supported, call the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-isformatsupported">IMediaSeeking::IsFormatSupported</a> method. If a format is supported, you can switch to that format by calling <code>SetTimeFormat</code>. Only one time format is active at any one time.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-gettimeformat">IMediaSeeking::GetTimeFormat</a>



<a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-querypreferredformat">IMediaSeeking::QueryPreferredFormat</a>