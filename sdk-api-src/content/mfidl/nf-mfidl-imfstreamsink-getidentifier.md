---
UID: NF:mfidl.IMFStreamSink.GetIdentifier
title: IMFStreamSink::GetIdentifier (mfidl.h)
description: Retrieves the stream identifier for this stream sink.
helpviewer_keywords: ["GetIdentifier","GetIdentifier method [Media Foundation]","GetIdentifier method [Media Foundation]","IMFStreamSink interface","IMFStreamSink interface [Media Foundation]","GetIdentifier method","IMFStreamSink.GetIdentifier","IMFStreamSink::GetIdentifier","af4855f6-36fa-4949-8b93-9e630a12e71b","mf.imfstreamsink_getidentifier","mfidl/IMFStreamSink::GetIdentifier"]
old-location: mf\imfstreamsink_getidentifier.htm
tech.root: mf
ms.assetid: af4855f6-36fa-4949-8b93-9e630a12e71b
ms.date: 12/05/2018
ms.keywords: GetIdentifier, GetIdentifier method [Media Foundation], GetIdentifier method [Media Foundation],IMFStreamSink interface, IMFStreamSink interface [Media Foundation],GetIdentifier method, IMFStreamSink.GetIdentifier, IMFStreamSink::GetIdentifier, af4855f6-36fa-4949-8b93-9e630a12e71b, mf.imfstreamsink_getidentifier, mfidl/IMFStreamSink::GetIdentifier
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
 - IMFStreamSink::GetIdentifier
 - mfidl/IMFStreamSink::GetIdentifier
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
 - IMFStreamSink.GetIdentifier
---

# IMFStreamSink::GetIdentifier


## -description

Retrieves the stream identifier for this stream sink.

## -parameters

### -param pdwIdentifier [out]

Receives the stream identifier. If this stream sink was added by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a>, the stream identifier is in the <i>dwStreamSinkIdentifier</i> parameter of that method. Otherwise, the media sink defines the identifier.

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
<dt><b>MF_E_STREAMSINK_REMOVED</b></dt>
</dl>
</td>
<td width="60%">
This stream was removed from the media sink and is no longer valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>