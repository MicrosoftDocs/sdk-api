---
UID: NF:mfidl.IMFSourceResolver.BeginCreateObjectFromURL
title: IMFSourceResolver::BeginCreateObjectFromURL (mfidl.h)
description: Begins an asynchronous request to create a media source or a byte stream from a URL.
helpviewer_keywords: ["BeginCreateObjectFromURL","BeginCreateObjectFromURL method [Media Foundation]","BeginCreateObjectFromURL method [Media Foundation]","IMFSourceResolver interface","IMFSourceResolver interface [Media Foundation]","BeginCreateObjectFromURL method","IMFSourceResolver.BeginCreateObjectFromURL","IMFSourceResolver::BeginCreateObjectFromURL","bc97c1fb-d23a-4887-b6ac-0751c254a405","mf.imfsourceresolver_begincreateobjectfromurl","mfidl/IMFSourceResolver::BeginCreateObjectFromURL"]
old-location: mf\imfsourceresolver_begincreateobjectfromurl.htm
tech.root: mf
ms.assetid: bc97c1fb-d23a-4887-b6ac-0751c254a405
ms.date: 12/05/2018
ms.keywords: BeginCreateObjectFromURL, BeginCreateObjectFromURL method [Media Foundation], BeginCreateObjectFromURL method [Media Foundation],IMFSourceResolver interface, IMFSourceResolver interface [Media Foundation],BeginCreateObjectFromURL method, IMFSourceResolver.BeginCreateObjectFromURL, IMFSourceResolver::BeginCreateObjectFromURL, bc97c1fb-d23a-4887-b6ac-0751c254a405, mf.imfsourceresolver_begincreateobjectfromurl, mfidl/IMFSourceResolver::BeginCreateObjectFromURL
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
 - IMFSourceResolver::BeginCreateObjectFromURL
 - mfidl/IMFSourceResolver::BeginCreateObjectFromURL
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
 - IMFSourceResolver.BeginCreateObjectFromURL
---

# IMFSourceResolver::BeginCreateObjectFromURL


## -description

Begins an asynchronous request to create a media source or a byte stream from a URL.

## -parameters

### -param pwszURL [in]

Null-terminated string that contains the URL to resolve.

### -param dwFlags [in]

Bitwise OR of flags. See <a href="/windows/desktop/medfound/source-resolver-flags">Source Resolver Flags</a>.

### -param pProps [in]

Pointer to the <b>IPropertyStore</b> interface of a property store. The method passes the property store to the scheme handler or byte-stream handler that creates the object. The handler can use the property store to configure the object. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/medfound/configuring-a-media-source">Configuring a Media Source</a>.

### -param ppIUnknownCancelCookie [out]

Receives an <b>IUnknown</b> pointer or the value <b>NULL</b>. If the value is not <b>NULL</b>, you can cancel the asynchronous operation by passing this pointer to the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-cancelobjectcreation">IMFSourceResolver::CancelObjectCreation</a> method. The caller must release the interface. This parameter can be <b>NULL</b>.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

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
<dt><b>MF_E_UNSUPPORTED_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
The URL scheme is not supported.

</td>
</tr>
</table>

## -remarks

The <i>dwFlags</i> parameter must contain either the MF_RESOLUTION_MEDIASOURCE flag or the MF_RESOLUTION_BYTESTREAM flag, but should not contain both.

For local files, you can pass the file name in the <i>pwszURL</i> parameter; the <code>file:</code> scheme is not required.

When the operation completes, the source resolver calls the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method. The <b>Invoke</b> method should call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl">IMFSourceResolver::EndCreateObjectFromURL</a> to get a pointer to the object that was created.

The usage of the <i>pProps</i> parameter depends on the implementation of the media source.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a>



<a href="/windows/desktop/medfound/source-resolver">Source Resolver</a>