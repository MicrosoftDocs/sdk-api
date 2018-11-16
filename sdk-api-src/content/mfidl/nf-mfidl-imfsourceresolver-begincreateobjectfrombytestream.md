---
UID: NF:mfidl.IMFSourceResolver.BeginCreateObjectFromByteStream
title: IMFSourceResolver::BeginCreateObjectFromByteStream
author: windows-sdk-content
description: Begins an asynchronous request to create a media source from a byte stream.
old-location: mf\imfsourceresolver_begincreateobjectfrombytestream.htm
tech.root: medfound
ms.assetid: 6e218b93-4855-40dd-96cc-c4ee02792c14
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 6e218b93-4855-40dd-96cc-c4ee02792c14, BeginCreateObjectFromByteStream, BeginCreateObjectFromByteStream method [Media Foundation], BeginCreateObjectFromByteStream method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],BeginCreateObjectFromByteStream method, IMFSourceResolver.BeginCreateObjectFromByteStream, IMFSourceResolver::BeginCreateObjectFromByteStream, mf.imfsourceresolver_begincreateobjectfrombytestream, mfidl/IMFSourceResolver::BeginCreateObjectFromByteStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSourceResolver.BeginCreateObjectFromByteStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFSourceResolver.BeginCreateObjectFromByteStream
: 
---

# IMFSourceResolver::BeginCreateObjectFromByteStream


## -description



Begins an asynchronous request to create a media source from a byte stream.




## -parameters




### -param pByteStream [in]

A pointer to the byte stream's <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface.
          


### -param pwszURL [in]

A null-terminated string that contains the original URL of the byte stream. This parameter can be <b>NULL</b>.
          


### -param dwFlags [in]

A bitwise <b>OR</b> of one or more flags. See <a href="https://msdn.microsoft.com/fe0b9090-5d2a-41a4-a806-57c874d3b3a2">Source Resolver Flags</a>.
          


### -param pProps [in]

A pointer to the <b>IPropertyStore</b> interface of a property store. The method passes the property store to the byte-stream handler. The byte-stream handler can use the property store to configure the media source. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/1378bbe6-be94-4be1-b428-5ec58dabd1fa">Configuring a Media Source</a>.
          


### -param ppIUnknownCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="https://msdn.microsoft.com/6a30ac92-a281-4293-8975-987fa25a5318">IMFSourceResolver::CancelObjectCreation</a> method. The caller must release the interface. This parameter can be <b>NULL</b>.
          


### -param pCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.
          


### -param punkState [in]

A oointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.
          


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
<dt><b>MF_E_SOURCERESOLVER_MUTUALLY_EXCLUSIVE_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwFlags</i> parameter contains mutually exclusive flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_BYTESTREAM_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The byte stream is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BYTESTREAM_NOT_SEEKABLE</b></dt>
</dl>
</td>
<td width="60%">
The byte stream does not support seeking.

</td>
</tr>
</table>
 




## -remarks



The <i>dwFlags</i> parameter must contain the <b>MF_RESOLUTION_MEDIASOURCE</b> flag and should not contain the <b>MF_RESOLUTION_BYTESTREAM</b> flag.

The source resolver attempts to find one or more byte-stream handlers for the byte stream, based on the file name extension of the URL, or the MIME type of the byte stream (or both). The URL is specified in the optional <i>pwszURL</i> parameter, and the MIME type may be specified in the <a href="https://msdn.microsoft.com/bcf86ece-2673-4ed8-98fd-cd0e2154b4a8">MF_BYTESTREAM_CONTENT_TYPE</a> attribute on the byte stream. Byte-stream handlers are registered by file name extension or MIME type, or both, as described in <a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>. The caller should specify at least one of these values.

When the operation completes, the source resolver calls the <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> method. The <b>Invoke</b> method should call <a href="https://msdn.microsoft.com/54532c0e-772b-45b6-95a3-5959023b9bc8">IMFSourceResolver::EndCreateObjectFromByteStream</a> to get a pointer to the media source.




## -see-also




<a href="https://msdn.microsoft.com/079c61c5-7a29-4411-840e-9349190726ac">IMFSourceResolver</a>



<a href="https://msdn.microsoft.com/93eecf10-308b-4bb4-92f9-fd32d6ecdb04">Source Resolver</a>
 

 

