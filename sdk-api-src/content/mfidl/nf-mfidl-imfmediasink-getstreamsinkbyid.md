---
UID: NF:mfidl.IMFMediaSink.GetStreamSinkById
title: IMFMediaSink::GetStreamSinkById (mfidl.h)
description: Gets a stream sink, specified by stream identifier.
helpviewer_keywords: ["267a8efc-6743-48ca-a1c4-da82f3770419","GetStreamSinkById","GetStreamSinkById method [Media Foundation]","GetStreamSinkById method [Media Foundation]","IMFMediaSink interface","IMFMediaSink interface [Media Foundation]","GetStreamSinkById method","IMFMediaSink.GetStreamSinkById","IMFMediaSink::GetStreamSinkById","mf.imfmediasink_getstreamsinkbyid","mfidl/IMFMediaSink::GetStreamSinkById"]
old-location: mf\imfmediasink_getstreamsinkbyid.htm
tech.root: mf
ms.assetid: 267a8efc-6743-48ca-a1c4-da82f3770419
ms.date: 12/05/2018
ms.keywords: 267a8efc-6743-48ca-a1c4-da82f3770419, GetStreamSinkById, GetStreamSinkById method [Media Foundation], GetStreamSinkById method [Media Foundation],IMFMediaSink interface, IMFMediaSink interface [Media Foundation],GetStreamSinkById method, IMFMediaSink.GetStreamSinkById, IMFMediaSink::GetStreamSinkById, mf.imfmediasink_getstreamsinkbyid, mfidl/IMFMediaSink::GetStreamSinkById
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
 - IMFMediaSink::GetStreamSinkById
 - mfidl/IMFMediaSink::GetStreamSinkById
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
 - IMFMediaSink.GetStreamSinkById
---

# IMFMediaSink::GetStreamSinkById


## -description

Gets a stream sink, specified by stream identifier.

## -parameters

### -param dwStreamSinkIdentifier [in]

Stream identifier of the stream sink.

### -param ppStreamSink [out]

Receives a pointer to the stream's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a> interface. The caller must release the interface.

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
The stream identifier is not valid.

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
</table>

## -remarks

If you add a stream sink by calling the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a> method, the stream identifier is specified in the <i>dwStreamSinkIdentifier</i> parameter of that method. If the media sink has a fixed set of streams, the media sink assigns the stream identifiers.

To enumerate the streams by index number instead of stream identifier, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex">IMFMediaSink::GetStreamSinkByIndex</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>