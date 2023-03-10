---
UID: NF:mfidl.IMFSourceResolver.CreateObjectFromByteStream
title: IMFSourceResolver::CreateObjectFromByteStream (mfidl.h)
description: Creates a media source from a byte stream. This method is synchronous.
helpviewer_keywords: ["CreateObjectFromByteStream","CreateObjectFromByteStream method [Media Foundation]","CreateObjectFromByteStream method [Media Foundation]","IMFSourceResolver interface","IMFSourceResolver interface [Media Foundation]","CreateObjectFromByteStream method","IMFSourceResolver.CreateObjectFromByteStream","IMFSourceResolver::CreateObjectFromByteStream","e4a4aad5-0924-4251-b0da-6919ae010bf0","mf.imfsourceresolver_createobjectfrombytestream","mfidl/IMFSourceResolver::CreateObjectFromByteStream"]
old-location: mf\imfsourceresolver_createobjectfrombytestream.htm
tech.root: mf
ms.assetid: e4a4aad5-0924-4251-b0da-6919ae010bf0
ms.date: 12/05/2018
ms.keywords: CreateObjectFromByteStream, CreateObjectFromByteStream method [Media Foundation], CreateObjectFromByteStream method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],CreateObjectFromByteStream method, IMFSourceResolver.CreateObjectFromByteStream, IMFSourceResolver::CreateObjectFromByteStream, e4a4aad5-0924-4251-b0da-6919ae010bf0, mf.imfsourceresolver_createobjectfrombytestream, mfidl/IMFSourceResolver::CreateObjectFromByteStream
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
 - IMFSourceResolver::CreateObjectFromByteStream
 - mfidl/IMFSourceResolver::CreateObjectFromByteStream
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
 - IMFSourceResolver.CreateObjectFromByteStream
---

# IMFSourceResolver::CreateObjectFromByteStream


## -description

Creates a media source from a byte stream. This method is synchronous.

## -parameters

### -param pByteStream [in]

Pointer to the byte stream's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> interface.

### -param pwszURL [in]

Null-terminated string that contains the URL of the byte stream. The URL is optional and can be <b>NULL</b>. See Remarks for more information.

### -param dwFlags [in]

Bitwise <b>OR</b> of flags. See <a href="/windows/desktop/medfound/source-resolver-flags">Source Resolver Flags</a>.

### -param pProps [in]

Pointer to the <b>IPropertyStore</b> interface of a property store. The method passes the property store to the byte-stream handler. The byte-stream handler can use the property store to configure the media source. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/medfound/configuring-a-media-source">Configuring a Media Source</a>.

### -param pObjectType [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_object_type">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.

### -param ppObject [out]

Receives a pointer to the media source's <b>IUnknown</b> interface. The caller must release the interface.

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
This byte stream is not supported.
              

</td>
</tr>
</table>

## -remarks

The <i>dwFlags</i> parameter must contain the <b>MF_RESOLUTION_MEDIASOURCE</b> flag and should not contain the <b>MF_RESOLUTION_BYTESTREAM</b> flag.

The source resolver attempts to find one or more byte-stream handlers for the byte stream, based on the file name extension of the URL, or the MIME type of the byte stream (or both). The URL is specified in the optional <i>pwszURL</i> parameter, and the MIME type may be specified in the <a href="/windows/desktop/medfound/mf-bytestream-content-type-attribute">MF_BYTESTREAM_CONTENT_TYPE</a> attribute on the byte stream. Byte-stream handlers are registered by file name extension or MIME type, or both, as described in <a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>. The caller should specify at least one of these values (both if possible):

<ul>
<li>Specify the URL in the <i>pwszURL</i> parameter.
          </li>
<li>Specify the MIME type by setting the <a href="/windows/desktop/medfound/mf-bytestream-content-type-attribute">MF_BYTESTREAM_CONTENT_TYPE</a> attribute on the byte stream. (This attribute might be set already when you create the byte stream, depending on how the byte stream was created.)
          </li>
</ul>
<div class="alert"><b>Note</b>  This method cannot be called remotely.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a>



<a href="/windows/desktop/medfound/source-resolver">Source Resolver</a>