---
UID: NF:mfidl.IMFByteStreamHandler.EndCreateObject
title: IMFByteStreamHandler::EndCreateObject (mfidl.h)
description: Completes an asynchronous request to create a media source.
helpviewer_keywords: ["8fd9797a-8dfb-4e59-8bcb-52dc53b5bb2e","EndCreateObject","EndCreateObject method [Media Foundation]","EndCreateObject method [Media Foundation]","IMFByteStreamHandler interface","IMFByteStreamHandler interface [Media Foundation]","EndCreateObject method","IMFByteStreamHandler.EndCreateObject","IMFByteStreamHandler::EndCreateObject","mf.imfbytestreamhandler_endcreateobject","mfidl/IMFByteStreamHandler::EndCreateObject"]
old-location: mf\imfbytestreamhandler_endcreateobject.htm
tech.root: mf
ms.assetid: 8fd9797a-8dfb-4e59-8bcb-52dc53b5bb2e
ms.date: 12/05/2018
ms.keywords: 8fd9797a-8dfb-4e59-8bcb-52dc53b5bb2e, EndCreateObject, EndCreateObject method [Media Foundation], EndCreateObject method [Media Foundation],IMFByteStreamHandler interface, IMFByteStreamHandler interface [Media Foundation],EndCreateObject method, IMFByteStreamHandler.EndCreateObject, IMFByteStreamHandler::EndCreateObject, mf.imfbytestreamhandler_endcreateobject, mfidl/IMFByteStreamHandler::EndCreateObject
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
 - IMFByteStreamHandler::EndCreateObject
 - mfidl/IMFByteStreamHandler::EndCreateObject
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
 - IMFByteStreamHandler.EndCreateObject
---

# IMFByteStreamHandler::EndCreateObject


## -description

Completes an asynchronous request to create a media source.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a> method.

### -param pObjectType [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_object_type">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.

### -param ppObject [out]

Receives a pointer to the <b>IUnknown</b> interface of the media source. The caller must release the interface.

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
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was canceled. See <a href="/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation">IMFByteStreamHandler::CancelObjectCreation</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_CANNOT_PARSE_BYTESTREAM</b></dt>
</dl>
</td>
<td width="60%">
Unable to parse the byte stream.

</td>
</tr>
</table>

## -remarks

Call this method from inside the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler">IMFByteStreamHandler</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>