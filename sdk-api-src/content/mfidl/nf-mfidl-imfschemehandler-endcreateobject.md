---
UID: NF:mfidl.IMFSchemeHandler.EndCreateObject
title: IMFSchemeHandler::EndCreateObject (mfidl.h)
description: Completes an asynchronous request to create an object from a URL. (IMFSchemeHandler.EndCreateObject)
helpviewer_keywords: ["EndCreateObject","EndCreateObject method [Media Foundation]","EndCreateObject method [Media Foundation]","IMFSchemeHandler interface","IMFSchemeHandler interface [Media Foundation]","EndCreateObject method","IMFSchemeHandler.EndCreateObject","IMFSchemeHandler::EndCreateObject","e3f88904-c30f-4d40-ac79-c83b0a06f1fa","mf.imfschemehandler_endcreateobject","mfidl/IMFSchemeHandler::EndCreateObject"]
old-location: mf\imfschemehandler_endcreateobject.htm
tech.root: mf
ms.assetid: e3f88904-c30f-4d40-ac79-c83b0a06f1fa
ms.date: 12/05/2018
ms.keywords: EndCreateObject, EndCreateObject method [Media Foundation], EndCreateObject method [Media Foundation],IMFSchemeHandler interface, IMFSchemeHandler interface [Media Foundation],EndCreateObject method, IMFSchemeHandler.EndCreateObject, IMFSchemeHandler::EndCreateObject, e3f88904-c30f-4d40-ac79-c83b0a06f1fa, mf.imfschemehandler_endcreateobject, mfidl/IMFSchemeHandler::EndCreateObject
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
 - IMFSchemeHandler::EndCreateObject
 - mfidl/IMFSchemeHandler::EndCreateObject
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
 - IMFSchemeHandler.EndCreateObject
---

# IMFSchemeHandler::EndCreateObject


## -description

Completes an asynchronous request to create an object from a URL.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the Invoke method.

### -param pObjectType [out]

Receives a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_object_type">MF_OBJECT_TYPE</a> enumeration, specifying the type of object that was created.

### -param ppObject [out]

Receives a pointer to the <b>IUnknown</b> interface of the object. The caller must release the interface.

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
The operation was canceled.

</td>
</tr>
</table>

## -remarks

Call this method from inside the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler">IMFSchemeHandler</a>



<a href="/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>
