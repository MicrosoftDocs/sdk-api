---
UID: NF:mfidl.IMFStreamSink.GetMediaSink
title: IMFStreamSink::GetMediaSink (mfidl.h)
description: Retrieves the media sink that owns this stream sink.
helpviewer_keywords: ["799fb0ce-6a43-49c2-97cf-49c51d8f69cd","GetMediaSink","GetMediaSink method [Media Foundation]","GetMediaSink method [Media Foundation]","IMFStreamSink interface","IMFStreamSink interface [Media Foundation]","GetMediaSink method","IMFStreamSink.GetMediaSink","IMFStreamSink::GetMediaSink","mf.imfstreamsink_getmediasink","mfidl/IMFStreamSink::GetMediaSink"]
old-location: mf\imfstreamsink_getmediasink.htm
tech.root: mf
ms.assetid: 799fb0ce-6a43-49c2-97cf-49c51d8f69cd
ms.date: 12/05/2018
ms.keywords: 799fb0ce-6a43-49c2-97cf-49c51d8f69cd, GetMediaSink, GetMediaSink method [Media Foundation], GetMediaSink method [Media Foundation],IMFStreamSink interface, IMFStreamSink interface [Media Foundation],GetMediaSink method, IMFStreamSink.GetMediaSink, IMFStreamSink::GetMediaSink, mf.imfstreamsink_getmediasink, mfidl/IMFStreamSink::GetMediaSink
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
 - IMFStreamSink::GetMediaSink
 - mfidl/IMFStreamSink::GetMediaSink
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
 - IMFStreamSink.GetMediaSink
---

# IMFStreamSink::GetMediaSink


## -description

Retrieves the media sink that owns this stream sink.

## -parameters

### -param ppMediaSink [out]

Receives a pointer to the media sink's <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.

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