---
UID: NF:objbase.BindMoniker
title: BindMoniker function (objbase.h)
description: Locates an object by means of its moniker, activates the object if it is inactive, and retrieves a pointer to the specified interface on that object.
helpviewer_keywords: ["BindMoniker","BindMoniker function [COM]","_com_BindMoniker","com.bindmoniker","objbase/BindMoniker"]
old-location: com\bindmoniker.htm
tech.root: com
ms.assetid: 5a022c39-fc2c-458b-9dfe-fed1255d49a4
ms.date: 12/05/2018
ms.keywords: BindMoniker, BindMoniker function [COM], _com_BindMoniker, com.bindmoniker, objbase/BindMoniker
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BindMoniker
 - objbase/BindMoniker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - Ole32.dll
api_name:
 - BindMoniker
req.apiset: ext-ms-win-com-ole32-l1-1-5 (introduced in Windows 10, version 10.0.15063)
---

# BindMoniker function


## -description

Locates an object by means of its moniker, activates the object if it is inactive, and retrieves a pointer to the specified interface on that object.

## -parameters

### -param pmk [in]

A pointer to the object's moniker. See <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a>.

### -param grfOpt [in]

This parameter is reserved for future use and must be 0.

### -param iidResult [in]

The interface identifier to be used to communicate with the object.

### -param ppvResult [out]

The address of pointer variable that receives the interface pointer requested in <i>iidResult</i>. Upon successful return, *<i>ppvResult</i> contains the requested interface pointer. If an error occurs, *<i>ppvResult</i> is <b>NULL</b>. If the call is successful, the caller is responsible for releasing the pointer with a call to the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

This function can return the following error codes, or any of the error values returned by the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> method.

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
The object was located and activated, if necessary, and a pointer to the requested interface was returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MK_E_NOOBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object that the moniker object identified could not be found.

</td>
</tr>
</table>

## -remarks

<b>BindMoniker</b> is a helper function supplied as a convenient way for a client that has the moniker of an object to obtain a pointer to one of that object's interfaces. <b>BindMoniker</b> packages the following calls:


``` syntax
CreateBindCtx(0, &pbc);
pmk->BindToObject(pbc, NULL, riid, ppvObj);
```


<a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a> creates a bind context object that supports the system implementation of IBindContext. The pmk parameter is actually a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> implementation on a moniker object. This implementation's <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">BindToObject</a> method supplies the pointer to the requested interface pointer.

If you have several monikers to bind in quick succession and if you know that those monikers will activate the same object, it may be more efficient to call the <a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a> method directly, which enables you to use the same bind context object for all the monikers. See the <a href="/windows/desktop/api/objidl/nn-objidl-ibindctx">IBindCtx</a> interface for more information.

Container applications that allow their documents to contain linked objects are a special client that generally does not make direct calls to <a href="/windows/desktop/api/objidl/nn-objidl-imoniker">IMoniker</a> methods. Instead, the client manipulates the linked objects through the <a href="/windows/desktop/api/oleidl/nn-oleidl-iolelink">IOleLink</a> interface. The default handler implements this interface and calls the appropriate <b>IMoniker</b> methods as needed.

## -see-also

<a href="/windows/desktop/api/objbase/nf-objbase-createbindctx">CreateBindCtx</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imoniker-bindtoobject">IMoniker::BindToObject</a>
