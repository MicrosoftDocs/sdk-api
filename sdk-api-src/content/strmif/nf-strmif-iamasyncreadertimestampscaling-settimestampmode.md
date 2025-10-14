---
UID: NF:strmif.IAMAsyncReaderTimestampScaling.SetTimestampMode
title: IAMAsyncReaderTimestampScaling::SetTimestampMode (strmif.h)
description: Sets the filter's time-stamping mode.
helpviewer_keywords: ["FALSE","IAMAsyncReaderTimestampScaling interface [DirectShow]","SetTimestampMode method","IAMAsyncReaderTimestampScaling.SetTimestampMode","IAMAsyncReaderTimestampScaling::SetTimestampMode","SetTimestampMode","SetTimestampMode method [DirectShow]","SetTimestampMode method [DirectShow]","IAMAsyncReaderTimestampScaling interface","TRUE","dshow.iamasyncreadertimestampscaling_settimestampmode","strmif/IAMAsyncReaderTimestampScaling::SetTimestampMode"]
old-location: dshow\iamasyncreadertimestampscaling_settimestampmode.htm
tech.root: dshow
ms.assetid: 7f556e26-049d-4024-95a2-c899be1ef180
ms.date: 4/26/2023
ms.keywords: FALSE, IAMAsyncReaderTimestampScaling interface [DirectShow],SetTimestampMode method, IAMAsyncReaderTimestampScaling.SetTimestampMode, IAMAsyncReaderTimestampScaling::SetTimestampMode, SetTimestampMode, SetTimestampMode method [DirectShow], SetTimestampMode method [DirectShow],IAMAsyncReaderTimestampScaling interface, TRUE, dshow.iamasyncreadertimestampscaling_settimestampmode, strmif/IAMAsyncReaderTimestampScaling::SetTimestampMode
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
 - IAMAsyncReaderTimestampScaling::SetTimestampMode
 - strmif/IAMAsyncReaderTimestampScaling::SetTimestampMode
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
 - IAMAsyncReaderTimestampScaling.SetTimestampMode
---

# IAMAsyncReaderTimestampScaling::SetTimestampMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Sets the filter's time-stamping mode.

## -parameters

### -param fRaw [in]

Specifies the units for the source filter's time stamps.

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
 

The default value is <b>FALSE</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To support large files (greater than 850 GB), the downstream parser filter can call this method with the value <b>TRUE</b>. For backward compatibility, the default setting is <b>FALSE</b>. Call the method when the pins connect.

Applications should never call this method; doing so will cause the parser filter to misinterpret the time stamps.

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-iamasyncreadertimestampscaling">IAMAsyncReaderTimestampScaling</a>