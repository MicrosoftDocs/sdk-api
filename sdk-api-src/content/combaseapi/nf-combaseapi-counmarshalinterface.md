---
UID: NF:combaseapi.CoUnmarshalInterface
title: CoUnmarshalInterface function (combaseapi.h)
description: Initializes a newly created proxy using data written into the stream by a previous call to the CoMarshalInterface function, and returns an interface pointer to that proxy.
helpviewer_keywords: ["CoUnmarshalInterface","CoUnmarshalInterface function [COM]","_com_CoUnmarshalInterface","com.counmarshalinterface","combaseapi/CoUnmarshalInterface"]
old-location: com\counmarshalinterface.htm
tech.root: com
ms.assetid: d0eac0da-2f41-40c4-b756-31bc22752c17
ms.date: 12/05/2018
ms.keywords: CoUnmarshalInterface, CoUnmarshalInterface function [COM], _com_CoUnmarshalInterface, com.counmarshalinterface, combaseapi/CoUnmarshalInterface
req.header: combaseapi.h
req.include-header: Objbase.h
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
 - CoUnmarshalInterface
 - combaseapi/CoUnmarshalInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoUnmarshalInterface
---

# CoUnmarshalInterface function


## -description

Initializes a newly created proxy using data written into the stream by a previous call to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a> function, and returns an interface pointer to that proxy.

## -parameters

### -param pStm [in]

A pointer to the stream from which the interface is to be unmarshaled.

### -param riid [in]

A reference to the identifier of the interface to be unmarshaled. For <b>IID_NULL</b>, the returned interface is the one defined by the stream, objref.iid.

### -param ppv [out]

The address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppv</i> contains the requested interface pointer for the unmarshaled interface.

## -returns

This function can return the standard return value E_FAIL, errors returned by <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>, and the following values.

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
The interface pointer was unmarshaled successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pStm</i> is an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> function was not called on the current thread before this function was called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_OBJNOTCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The object application has been disconnected from the remoting system (for example, as a result of a call to the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-codisconnectobject">CoDisconnectObject</a> function).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
An error occurred reading the registration database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The final <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> of this function for the requested interface returned E_NOINTERFACE.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data.

</div>
<div> </div>
The <b>CoUnmarshalInterface</b> function performs the following tasks:

<ol>
<li>Reads from the stream the CLSID to be used to create an instance of the proxy.
</li>
<li>Gets an <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> pointer to the proxy that is to do the unmarshaling. If the object uses COM's default marshaling implementation, the pointer thus obtained is to an instance of the generic proxy object. If the marshaling is occurring between two threads in the same process, the pointer is to an instance of the in-process free threaded marshaler. If the object provides its own marshaling code, <b>CoUnmarshalInterface</b> calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function, passing the CLSID it read from the marshaling stream. <b>CoCreateInstance</b> creates an instance of the object's proxy and returns an <b>IMarshal</b> interface pointer to the proxy.</li>
<li>Using whichever IMarshal interface pointer it has acquired, the function then calls <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-unmarshalinterface">IMarshal::UnmarshalInterface</a> and, if appropriate, <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-releasemarshaldata">IMarshal::ReleaseMarshalData</a>. 
</li>
</ol>
The primary caller of this function is COM itself, from within interface proxies or stubs that unmarshal an interface pointer. There are, however, some situations in which you might call <b>CoUnmarshalInterface</b>. For example, if you are implementing a stub, your implementation would call <b>CoUnmarshalInterface</b> when the stub receives an interface pointer as a parameter in a method call.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imarshal-unmarshalinterface">IMarshal::UnmarshalInterface</a>