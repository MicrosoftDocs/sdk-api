---
UID: NF:mfidl.IMFMediaSink.RemoveStreamSink
title: IMFMediaSink::RemoveStreamSink (mfidl.h)
description: Removes a stream sink from the media sink.
helpviewer_keywords: ["IMFMediaSink interface [Media Foundation]","RemoveStreamSink method","IMFMediaSink.RemoveStreamSink","IMFMediaSink::RemoveStreamSink","RemoveStreamSink","RemoveStreamSink method [Media Foundation]","RemoveStreamSink method [Media Foundation]","IMFMediaSink interface","f99ee960-7fea-4867-bc24-d7e1d6fcafa5","mf.imfmediasink_removestreamsink","mfidl/IMFMediaSink::RemoveStreamSink"]
old-location: mf\imfmediasink_removestreamsink.htm
tech.root: mf
ms.assetid: f99ee960-7fea-4867-bc24-d7e1d6fcafa5
ms.date: 12/05/2018
ms.keywords: IMFMediaSink interface [Media Foundation],RemoveStreamSink method, IMFMediaSink.RemoveStreamSink, IMFMediaSink::RemoveStreamSink, RemoveStreamSink, RemoveStreamSink method [Media Foundation], RemoveStreamSink method [Media Foundation],IMFMediaSink interface, f99ee960-7fea-4867-bc24-d7e1d6fcafa5, mf.imfmediasink_removestreamsink, mfidl/IMFMediaSink::RemoveStreamSink
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
 - IMFMediaSink::RemoveStreamSink
 - mfidl/IMFMediaSink::RemoveStreamSink
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
 - IMFMediaSink.RemoveStreamSink
---

# IMFMediaSink::RemoveStreamSink


## -description

Removes a stream sink from the media sink.

## -parameters

### -param dwStreamSinkIdentifier [in]

Identifier of the stream to remove. The stream identifier is defined when you call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">IMFMediaSink::AddStreamSink</a> to add the stream sink.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
This particular stream sink cannot be removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The stream number is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The media sink has not been initialized.

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
<dt><b>MF_E_STREAMSINKS_FIXED</b></dt>
</dl>
</td>
<td width="60%">
This media sink has a fixed set of stream sinks. Stream sinks cannot be removed.

</td>
</tr>
</table>

## -remarks

After this method is called, the corresponding stream sink object is no longer valid. The <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex">IMFMediaSink::GetStreamSinkByIndex</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid">IMFMediaSink::GetStreamSinkById</a> methods will no longer return that stream sink. You can re-use the stream identifier if you add another stream (by calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink">AddStreamSink</a>).

Not all media sinks support this method. If the media sink does not support this method, the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics">IMFMediaSink::GetCharacteristics</a> method returns the MEDIASINK_FIXED_STREAMS flag.

In some cases, the media sink supports this method but does not allow every stream sink to be removed. (For example, it might not allow stream 0 to be removed.)

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>