---
UID: NF:combaseapi.CoGetStandardMarshal
title: CoGetStandardMarshal function (combaseapi.h)
description: Creates a default, or standard, marshaling object in either the client process or the server process, depending on the caller, and returns a pointer to that object's IMarshal implementation.
helpviewer_keywords: ["CoGetStandardMarshal","CoGetStandardMarshal function [COM]","_com_CoGetStandardMarshal","com.cogetstandardmarshal","combaseapi/CoGetStandardMarshal"]
old-location: com\cogetstandardmarshal.htm
tech.root: com
ms.assetid: 0cb74adc-e192-4ae5-9267-02c79e301681
ms.date: 12/05/2018
ms.keywords: CoGetStandardMarshal, CoGetStandardMarshal function [COM], _com_CoGetStandardMarshal, com.cogetstandardmarshal, combaseapi/CoGetStandardMarshal
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
 - CoGetStandardMarshal
 - combaseapi/CoGetStandardMarshal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-ole32-l1-1-0.dll
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - CoGetStandardMarshal
---

# CoGetStandardMarshal function


## -description

Creates a default, or standard, marshaling object in either the client process or the server process, depending on the caller, and returns a pointer to that object's <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> implementation.

## -parameters

### -param riid [in]

A reference to the identifier of the interface whose pointer is to be marshaled. This interface must be derived from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param pUnk [in]

A pointer to the interface to be marshaled.

### -param dwDestContext [in]

The destination context where the specified interface is to be unmarshaled. Values come from the enumeration <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshctx">MSHCTX</a>. Unmarshaling can occur either in another apartment of the current process (MSHCTX_INPROC) or in another process on the same computer as the current process (MSHCTX_LOCAL).

### -param pvDestContext [in, optional]

This parameter is reserved and must be <b>NULL</b>.

### -param mshlflags [in]

Indicates whether the data to be marshaled is to be transmitted back to the client process (the normal case) or written to a global table where it can be retrieved by multiple clients. Values come from the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshlflags">MSHLFLAGS</a> enumeration.

### -param ppMarshal [out]

The address of <b>IMarshal*</b> pointer variable that receives the interface pointer to the standard marshaler.

## -returns

This function can return the standard return values E_FAIL, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> instance was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
Before this function can be called, the <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> function must be called on the current thread.

</td>
</tr>
</table>

## -remarks

The <b>CoGetStandardMarshal</b> function creates a default, or standard, marshaling object in either the client process or the server process, as may be necessary, and returns that object's <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> pointer to the caller. If you implement <b>IMarshal</b>, you may want your implementation to call <b>CoGetStandardMarshal</b> as a way of delegating to COM's default implementation any destination contexts that you do not fully understand or want to handle. Otherwise, you can ignore this function, which COM calls as part of its internal marshaling procedures.

When the COM library in the client process receives a marshaled interface pointer, it looks for a CLSID to be used in creating a proxy for the purposes of unmarshaling the packet. If the packet does not contain a CLSID for the proxy, COM calls <b>CoGetStandardMarshal</b>, passing a <b>NULL</b><i>pUnk</i> value. This function creates a standard proxy in the client process and returns a pointer to that proxy's implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>. COM uses this pointer to call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a> to retrieve the pointer to the requested interface.

If your OLE server application's implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> calls <b>CoGetStandardMarshal</b>, you should pass both the IID of (<i>riid</i>), and a pointer to (<i>pUnk</i>), the interface being requested.



This function performs the following tasks: 

<ol>
<li>Determines whether pUnk is <b>NULL</b>.</li>
<li>If <i>pUnk</i> is <b>NULL</b>, creates a standard interface proxy in the client process for the specified <i>riid</i> and returns the proxy's <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> pointer.
</li>
<li>If <i>pUnk</i> is not <b>NULL</b>, checks to see if a marshaler for the object already exists, creates a new one if necessary, and returns the marshaler's <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> pointer.</li>
</ol>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>