---
UID: NF:strmif.IMediaSeeking.GetPositions
title: IMediaSeeking::GetPositions (strmif.h)
description: The GetPositions method retrieves the current position and the stop position, relative to the total duration of the stream.
helpviewer_keywords: ["GetPositions","GetPositions method [DirectShow]","GetPositions method [DirectShow]","IMediaSeeking interface","IMediaSeeking interface [DirectShow]","GetPositions method","IMediaSeeking.GetPositions","IMediaSeeking::GetPositions","IMediaSeekingGetPositions","dshow.imediaseeking_getpositions","strmif/IMediaSeeking::GetPositions"]
old-location: dshow\imediaseeking_getpositions.htm
tech.root: dshow
ms.assetid: 1b267c02-ec2d-4251-aac7-f2f711b16062
ms.date: 4/26/2023
ms.keywords: GetPositions, GetPositions method [DirectShow], GetPositions method [DirectShow],IMediaSeeking interface, IMediaSeeking interface [DirectShow],GetPositions method, IMediaSeeking.GetPositions, IMediaSeeking::GetPositions, IMediaSeekingGetPositions, dshow.imediaseeking_getpositions, strmif/IMediaSeeking::GetPositions
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
 - IMediaSeeking::GetPositions
 - strmif/IMediaSeeking::GetPositions
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
 - IMediaSeeking.GetPositions
---

# IMediaSeeking::GetPositions


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetPositions</code> method retrieves the current position and the stop position, relative to the total duration of the stream.

## -parameters

### -param pCurrent [out]

Pointer to a variable that receives the current position, in units of the current time format.

### -param pStop [out]

Pointer to a variable that receives the stop position, in units of the current time format.

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
</table>

## -remarks

The current position and the stop position are both relative to the original stream, and are independent of the playback rate.

The returned values are expressed in the current time format. The default time format is <a href="/windows/desktop/DirectShow/reference-time">REFERENCE_TIME</a> units (100 nanoseconds). To change time formats, use the <a href="/windows/desktop/api/strmif/nf-strmif-imediaseeking-settimeformat">IMediaSeeking::SetTimeFormat</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking Interface</a>