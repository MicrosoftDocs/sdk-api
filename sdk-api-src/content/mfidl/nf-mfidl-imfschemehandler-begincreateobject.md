---
UID: NF:mfidl.IMFSchemeHandler.BeginCreateObject
title: IMFSchemeHandler::BeginCreateObject (mfidl.h)
description: Begins an asynchronous request to create an object from a URL.When the Source Resolver creates a media source from a URL, it passes the request to a scheme handler.
helpviewer_keywords: ["78858e8c-0eb3-4b62-84f0-76e9dff0e3ce","BeginCreateObject","BeginCreateObject method [Media Foundation]","BeginCreateObject method [Media Foundation]","IMFSchemeHandler interface","IMFSchemeHandler interface [Media Foundation]","BeginCreateObject method","IMFSchemeHandler.BeginCreateObject","IMFSchemeHandler::BeginCreateObject","mf.imfschemehandler_begincreateobject","mfidl/IMFSchemeHandler::BeginCreateObject"]
old-location: mf\imfschemehandler_begincreateobject.htm
tech.root: mf
ms.assetid: 78858e8c-0eb3-4b62-84f0-76e9dff0e3ce
ms.date: 12/05/2018
ms.keywords: 78858e8c-0eb3-4b62-84f0-76e9dff0e3ce, BeginCreateObject, BeginCreateObject method [Media Foundation], BeginCreateObject method [Media Foundation],IMFSchemeHandler interface, IMFSchemeHandler interface [Media Foundation],BeginCreateObject method, IMFSchemeHandler.BeginCreateObject, IMFSchemeHandler::BeginCreateObject, mf.imfschemehandler_begincreateobject, mfidl/IMFSchemeHandler::BeginCreateObject
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
 - IMFSchemeHandler::BeginCreateObject
 - mfidl/IMFSchemeHandler::BeginCreateObject
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
 - IMFSchemeHandler.BeginCreateObject
---

# IMFSchemeHandler::BeginCreateObject


## -description

Begins an asynchronous request to create an object from a URL.

When the <a href="/windows/desktop/medfound/source-resolver">Source Resolver</a> creates a media source from a URL, it passes the request to a scheme handler. The scheme handler might create a media source directly from the URL, or it might return a byte stream. If it returns a byte stream, the source resolver use a byte-stream handler to create the media source from the byte stream.

## -parameters

### -param pwszURL [in]

A null-terminated string that contains the URL to resolve.

### -param dwFlags [in]

A bitwise <b>OR</b> of one or more flags. See <a href="/windows/desktop/medfound/source-resolver-flags">Source Resolver Flags</a>.

### -param pProps [in]

A pointer to the <b>IPropertyStore</b> interface of a property store. The scheme handler can use this property store to configure the object. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/medfound/configuring-a-media-source">Configuring a Media Source</a>.

### -param ppIUnknownCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-cancelobjectcreation">IMFSchemeHandler::CancelObjectCreation</a> method. The caller must release the interface. This parameter can be <b>NULL</b>, in which case the <b>IUnknown</b> pointer is not returned to the caller.

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param punkState [in]

A pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot open the URL with the requested access (read or write).
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_BYTESTREAM_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Unsupported byte stream type.
              

</td>
</tr>
</table>

## -remarks

The <i>dwFlags</i> parameter must contain the <b>MF_RESOLUTION_MEDIASOURCE</b> flag or the <b>MF_RESOLUTION_BYTESTREAM</b> flag. If the <b>MF_RESOLUTION_MEDIASOURCE</b> flag is set, the scheme handler might create the media source directly from the URL, or it might create a byte stream. The type of object is returned in the <i>pObjectType</i> parameter of the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-endcreateobject">IMFSchemeHandler::EndCreateObject</a> method. If the scheme handler returns a byte stream, the source resolver will pass the byte stream to a byte-stream handler, which will create the media source from the byte stream.

If the <b>MF_RESOLUTION_BYTESTREAM</b> flag is set, the scheme handler will attempt to create a byte stream from the URL. However, if the scheme handler is designed to create a media source directly, rather than a byte stream, the method will fail.

The following table summarizes the behavior of these two flags when passed to this method:

<table>
<tr>
<th>Flag</th>
<th>Object created</th>
</tr>
<tr>
<td><b>MF_RESOLUTION_MEDIASOURCE</b></td>
<td>Media source or byte stream</td>
</tr>
<tr>
<td><b>MF_RESOLUTION_BYTESTREAM</b></td>
<td>Byte stream</td>
</tr>
</table>
 

The <b>MF_RESOLUTION_MEDIASOURCE</b> and <b>MF_RESOLUTION_BYTESTREAM</b> flags can be combined, although in this case it is redundant.

When the operation completes, the scheme handler calls the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method. The Invoke method should call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-endcreateobject">IMFSchemeHandler::EndCreateObject</a> to get a pointer to the created object.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler">IMFSchemeHandler</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>