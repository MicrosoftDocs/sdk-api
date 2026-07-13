---
UID: NF:strmif.IAMAsyncReaderTimestampScaling.GetTimestampMode
title: IAMAsyncReaderTimestampScaling::GetTimestampMode (strmif.h)
description: Gets the filter's time-stamping mode.
helpviewer_keywords: ["FALSE","GetTimestampMode","GetTimestampMode method [DirectShow]","GetTimestampMode method [DirectShow]","IAMAsyncReaderTimestampScaling interface","IAMAsyncReaderTimestampScaling interface [DirectShow]","GetTimestampMode method","IAMAsyncReaderTimestampScaling.GetTimestampMode","IAMAsyncReaderTimestampScaling::GetTimestampMode","TRUE","dshow.iamasyncreadertimestampscaling_gettimestampmode","strmif/IAMAsyncReaderTimestampScaling::GetTimestampMode"]
old-location: dshow\iamasyncreadertimestampscaling_gettimestampmode.htm
tech.root: dshow
ms.assetid: 2fbadd9d-e741-482f-9ff1-655b149fec49
ms.date: 4/26/2023
ms.keywords: FALSE, GetTimestampMode, GetTimestampMode method [DirectShow], GetTimestampMode method [DirectShow],IAMAsyncReaderTimestampScaling interface, IAMAsyncReaderTimestampScaling interface [DirectShow],GetTimestampMode method, IAMAsyncReaderTimestampScaling.GetTimestampMode, IAMAsyncReaderTimestampScaling::GetTimestampMode, TRUE, dshow.iamasyncreadertimestampscaling_gettimestampmode, strmif/IAMAsyncReaderTimestampScaling::GetTimestampMode
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMAsyncReaderTimestampScaling::GetTimestampMode
 - strmif/IAMAsyncReaderTimestampScaling::GetTimestampMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMAsyncReaderTimestampScaling.GetTimestampMode
---

# IAMAsyncReaderTimestampScaling::GetTimestampMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Gets the filter's time-stamping mode.

## -parameters

### -param pfRaw [out]

Receives a Boolean value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Time stamps are in units of bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Time stamps are in units of bytes × 10000000. To get the offset in bytes, divide the sample time by 10000000.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamasyncreadertimestampscaling">IAMAsyncReaderTimestampScaling</a>