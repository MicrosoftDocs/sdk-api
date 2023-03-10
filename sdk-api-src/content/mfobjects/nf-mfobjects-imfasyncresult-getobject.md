---
UID: NF:mfobjects.IMFAsyncResult.GetObject
title: IMFAsyncResult::GetObject (mfobjects.h)
description: Returns an object associated with the asynchronous operation. The type of object, if any, depends on the asynchronous method that was called. (IMFAsyncResult.GetObject)
helpviewer_keywords: ["GetObject","GetObject method [Media Foundation]","GetObject method [Media Foundation]","IMFAsyncResult interface","IMFAsyncResult interface [Media Foundation]","GetObject method","IMFAsyncResult.GetObject","IMFAsyncResult::GetObject","b4b871ff-370d-4a37-9fe4-91d1805890eb","mf.imfasyncresult_getobject","mfobjects/IMFAsyncResult::GetObject"]
old-location: mf\imfasyncresult_getobject.htm
tech.root: mf
ms.assetid: b4b871ff-370d-4a37-9fe4-91d1805890eb
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Media Foundation], GetObject method [Media Foundation],IMFAsyncResult interface, IMFAsyncResult interface [Media Foundation],GetObject method, IMFAsyncResult.GetObject, IMFAsyncResult::GetObject, b4b871ff-370d-4a37-9fe4-91d1805890eb, mf.imfasyncresult_getobject, mfobjects/IMFAsyncResult::GetObject
req.header: mfobjects.h
req.include-header: Mfidl.h
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
 - IMFAsyncResult::GetObject
 - mfobjects/IMFAsyncResult::GetObject
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
 - IMFAsyncResult.GetObject
---

# IMFAsyncResult::GetObject


## -description

Returns an object associated with the asynchronous operation. The type of object, if any, depends on the asynchronous method that was called.

## -parameters

### -param ppObject [out]

Receives a pointer to the object's <b>IUnknown</b> interface. If no object is associated with the operation, this parameter receives the value <b>NULL</b>. If the value is not <b>NULL</b>, the caller must release the interface.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
There is no object associated with this asynchronous result.

</td>
</tr>
</table>

## -remarks

Typically, this object is used by the component that implements the asynchronous method. It provides a way for the function that invokes the callback to pass information to the asynchronous <b>End...</b> method that completes the operation.

If you are implementing an asynchronous method, you can set the object through the <i>punkObject</i> parameter of the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult">MFCreateAsyncResult</a> function.

If the asynchronous result object's internal <b>IUnknown</b> pointer is <b>NULL</b>, the method returns <b>E_POINTER</b>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/asynchronous-callback-methods">Asynchronous Callback Methods</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a>
