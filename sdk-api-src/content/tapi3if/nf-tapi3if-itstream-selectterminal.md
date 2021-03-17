---
UID: NF:tapi3if.ITStream.SelectTerminal
title: ITStream::SelectTerminal (tapi3if.h)
description: The SelectTerminal method selects an ITTerminal object onto the stream.
helpviewer_keywords: ["ITStream interface [TAPI 2.2]","SelectTerminal method","ITStream.SelectTerminal","ITStream::SelectTerminal","SelectTerminal","SelectTerminal method [TAPI 2.2]","SelectTerminal method [TAPI 2.2]","ITStream interface","_tapi3_itstream_selectterminal","tapi3.itstream_selectterminal","tapi3if/ITStream::SelectTerminal"]
old-location: tapi3\itstream_selectterminal.htm
tech.root: tapi3
ms.assetid: ecc4c7eb-c278-457a-b54e-5f1e582e22bf
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],SelectTerminal method, ITStream.SelectTerminal, ITStream::SelectTerminal, SelectTerminal, SelectTerminal method [TAPI 2.2], SelectTerminal method [TAPI 2.2],ITStream interface, _tapi3_itstream_selectterminal, tapi3.itstream_selectterminal, tapi3if/ITStream::SelectTerminal
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ITStream::SelectTerminal
 - tapi3if/ITStream::SelectTerminal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITStream.SelectTerminal
---

# ITStream::SelectTerminal


## -description

The 
<b>SelectTerminal</b> method selects an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> object onto the stream.

## -parameters

### -param pTerminal [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface of selected terminal.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminal</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_MAXTERMINALS</b></dt>
</dl>
</td>
<td width="60%">
Multiple terminals have been selected on the stream, but media mixing or splitting is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALIDTERMINAL</b></dt>
</dl>
</td>
<td width="60%">
The terminal selected is not valid.

</td>
</tr>
</table>

## -remarks

Terminals can be selected at any time, irrespective of whether the transport is in a state that allows it to stream media. If the transport is in a state that allows it to stream media, and the application has not successfully invoked 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-pausestream">ITStream::PauseStream</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">ITStream::StopStream</a> on the stream, or has successfully invoked 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">ITStream::StartStream</a> for this stream more recently than it has successfully invoked <b>ITStream::PauseStream</b> or <b>ITStream::StopStream</b> for this stream, then streaming starts automatically as soon as the terminal is selected. If a terminal is selected on the stream before the transport enters a state in which it can stream media, and no subsequent calls to 
<b>StopStream</b> or 
<b>PauseStream</b> are made, then the stream starts automatically when the transport enters a state in which it can stream media.

The CME_STREAM_ACTIVE event is generated when streaming actually starts, which may be later than the 
<b>SelectTerminal</b> call. The CME_STREAM_FAIL or CME_TERMINAL_FAIL event is generated when streaming actually fails, which may also be later than the 
<b>SelectTerminal</b> call.

A terminal can be selected onto a stream only if the results of 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminal-get_mediatype">ITTerminal::get_MediaType</a> match 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_mediatype">ITStream::get_MediaType</a>. In addition, some MSPs may require a match between 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminal-get_direction">ITTerminal::get_Direction</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_direction">ITStream::get_Direction</a>, although the interface does not enforce this.

Some MSPs may not allow more than a certain number of terminals, typically one, to be simultaneously selected on the same stream, but the interface itself does not enforce any such restriction. Selecting multiple terminals at one time on the same stream is useful, for example, to allow recording of an incoming audio stream to a file while listening to the stream on a pair of speakers.

A given terminal can be selected onto only one stream.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>