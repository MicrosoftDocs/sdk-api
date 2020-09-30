---
UID: NF:mfidl.IMFStreamSink.GetMediaTypeHandler
title: IMFStreamSink::GetMediaTypeHandler (mfidl.h)
description: Retrieves the media type handler for the stream sink. You can use the media type handler to find which formats the stream supports, and to set the media type on the stream.
helpviewer_keywords: ["819d06b1-6b52-4496-bed8-a08b8f0b6153","GetMediaTypeHandler","GetMediaTypeHandler method [Media Foundation]","GetMediaTypeHandler method [Media Foundation]","IMFStreamSink interface","IMFStreamSink interface [Media Foundation]","GetMediaTypeHandler method","IMFStreamSink.GetMediaTypeHandler","IMFStreamSink::GetMediaTypeHandler","mf.imfstreamsink_getmediatypehandler","mfidl/IMFStreamSink::GetMediaTypeHandler"]
old-location: mf\imfstreamsink_getmediatypehandler.htm
tech.root: mf
ms.assetid: 819d06b1-6b52-4496-bed8-a08b8f0b6153
ms.date: 12/05/2018
ms.keywords: 819d06b1-6b52-4496-bed8-a08b8f0b6153, GetMediaTypeHandler, GetMediaTypeHandler method [Media Foundation], GetMediaTypeHandler method [Media Foundation],IMFStreamSink interface, IMFStreamSink interface [Media Foundation],GetMediaTypeHandler method, IMFStreamSink.GetMediaTypeHandler, IMFStreamSink::GetMediaTypeHandler, mf.imfstreamsink_getmediatypehandler, mfidl/IMFStreamSink::GetMediaTypeHandler
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
 - IMFStreamSink::GetMediaTypeHandler
 - mfidl/IMFStreamSink::GetMediaTypeHandler
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
 - IMFStreamSink.GetMediaTypeHandler
---

# IMFStreamSink::GetMediaTypeHandler


## -description

Retrieves the media type handler for the stream sink. You can use the media type handler to find which formats the stream supports, and to set the media type on the stream.

## -parameters

### -param ppHandler [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler">IMFMediaTypeHandler</a> interface. The caller must release the interface.

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

## -remarks

If the stream sink currently does not support any media types, this method returns a media type handler that fails any calls to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype">IMFMediaTypeHandler::GetCurrentMediaType</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported">IMFMediaTypeHandler::IsMediaTypeSupported</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a>



<a href="/windows/desktop/medfound/media-sinks">Media Sinks</a>