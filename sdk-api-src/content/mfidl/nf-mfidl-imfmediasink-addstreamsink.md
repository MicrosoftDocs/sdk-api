---
UID: NF:mfidl.IMFMediaSink.AddStreamSink
title: IMFMediaSink::AddStreamSink (mfidl.h)
description: Adds a new stream sink to the media sink.
helpviewer_keywords: ["1b05ef87-5559-4310-942c-54ab113eb42d","AddStreamSink","AddStreamSink method [Media Foundation]","AddStreamSink method [Media Foundation]","IMFMediaSink interface","IMFMediaSink interface [Media Foundation]","AddStreamSink method","IMFMediaSink.AddStreamSink","IMFMediaSink::AddStreamSink","mf.imfmediasink_addstreamsink","mfidl/IMFMediaSink::AddStreamSink"]
old-location: mf\imfmediasink_addstreamsink.htm
tech.root: mf
ms.assetid: 1b05ef87-5559-4310-942c-54ab113eb42d
ms.date: 12/05/2018
ms.keywords: 1b05ef87-5559-4310-942c-54ab113eb42d, AddStreamSink, AddStreamSink method [Media Foundation], AddStreamSink method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],AddStreamSink method, IMFMediaSink.AddStreamSink, IMFMediaSink::AddStreamSink, mf.imfmediasink_addstreamsink, mfidl/IMFMediaSink::AddStreamSink
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaSink::AddStreamSink
 - mfidl/IMFMediaSink::AddStreamSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaSink.AddStreamSink
---

# IMFMediaSink::AddStreamSink


## -description

Adds a new stream sink to the media sink.

## -parameters

### -param dwStreamSinkIdentifier [in]

Identifier for the new stream. The value is arbitrary but must be unique.

### -param pMediaType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface, specifying the media type for the stream. This parameter can be <b>NULL</b>.

### -param ppStreamSink [out]

Receives a pointer to the new stream sink's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a> interface. The caller must release the interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The specified stream identifier is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown">Shutdown</a> method has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINK_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
There is already a stream sink with the same stream identifier.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_STREAMSINKS_FIXED</b></dt>
</dl>
</td>
<td width="60%">
This media sink has a fixed set of stream sinks. New stream sinks cannot be added.

</td>
</tr>
</table>

## -remarks

Not all media sinks support this method. If the media sink does not support this method, the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics">IMFMediaSink::GetCharacteristics</a> method returns the MEDIASINK_FIXED_STREAMS flag.

If <i>pMediaType</i> is <b>NULL</b>, use the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a> interface to set the media type. Call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler">IMFStreamSink::GetMediaTypeHandler</a> to get a pointer to the interface.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>