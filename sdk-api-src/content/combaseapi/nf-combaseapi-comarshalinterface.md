---
UID: NF:combaseapi.CoMarshalInterface
title: CoMarshalInterface function (combaseapi.h)
description: Writes into a stream the data required to initialize a proxy object in some client process.
helpviewer_keywords: ["CoMarshalInterface","CoMarshalInterface function [COM]","_com_CoMarshalInterface","com.comarshalinterface","combaseapi/CoMarshalInterface"]
old-location: com\comarshalinterface.htm
tech.root: com
ms.assetid: 04ca1217-eac1-43e2-b736-8d7522ce8592
ms.date: 12/05/2018
ms.keywords: CoMarshalInterface, CoMarshalInterface function [COM], _com_CoMarshalInterface, com.comarshalinterface, combaseapi/CoMarshalInterface
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
 - CoMarshalInterface
 - combaseapi/CoMarshalInterface
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
 - CoMarshalInterface
---

# CoMarshalInterface function


## -description

Writes into a stream the data required to initialize a proxy object in some client process.

## -parameters

### -param pStm [in]

A pointer to the stream to be used during marshaling. See <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>.

### -param riid [in]

A reference to the identifier of the interface to be marshaled. This interface must be derived from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param pUnk [in]

A pointer to the interface to be marshaled. This interface must be derived from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param dwDestContext [in]

The destination context where the specified interface is to be unmarshaled. The possible values come from the enumeration <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshctx">MSHCTX</a>. Currently, unmarshaling can occur in another apartment of the current process (MSHCTX_INPROC), in another process on the same computer as the current process (MSHCTX_LOCAL), or in a process on a different computer (MSHCTX_DIFFERENTMACHINE).

### -param pvDestContext [in, optional]

This parameter is reserved and must be <b>NULL</b>.

### -param mshlflags [in]

The flags that specify whether the data to be marshaled is to be transmitted back to the client process (the typical  case) or written to a global table, where it can be retrieved by multiple clients. The possible values come from the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshlflags">MSHLFLAGS</a> enumeration.

## -returns

This function can return the standard return values E_FAIL, E_OUTOFMEMORY, and E_UNEXPECTED, the stream-access error values returned by <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>, as well as the following values.

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
The <b>HRESULT</b> was marshaled successfully.

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
</table>

## -remarks

The <b>CoMarshalInterface</b> function marshals the interface referred to by riid on the object whose <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> implementation is pointed to by <i>pUnk</i>. To do so, the <b>CoMarshalInterface</b> function performs the following tasks:

<ol>
<li>
Queries the object for a pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> interface. If the object does not implement <b>IMarshal</b>, meaning that it relies on COM to provide marshaling support, <b>CoMarshalInterface</b> gets a pointer to COM's default implementation of <b>IMarshal</b>.

</li>
<li>
Gets the CLSID of the object's proxy by calling <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-getunmarshalclass">IMarshal::GetUnmarshalClass</a>, using whichever <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> interface pointer has been returned.

</li>
<li>
Writes the CLSID of the proxy to the stream to be used for marshaling.

</li>
<li>
Marshals the interface pointer by calling <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-marshalinterface">IMarshal::MarshalInterface</a>.

</li>
</ol>
The COM library in the client process calls the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a> function to extract the data and initialize the proxy. Before calling <b>CoUnmarshalInterface</b>, seek back to the original position in the stream.

If you are implementing existing COM interfaces or defining your own interfaces using the Microsoft Interface Definition Language (MIDL), the MIDL-generated proxies and stubs call <b>CoMarshalInterface</b> for you. If you are writing your own proxies and stubs, your proxy code and stub code should each call <b>CoMarshalInterface</b> to correctly marshal interface pointers. Calling <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> directly from your proxy and stub code is not recommended.

If you are writing your own implementation of <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>, and your proxy needs access to a private object, you can include an interface pointer to that object as part of the data you write to the stream. In such situations, if you want to use COM's default marshaling implementation when passing the interface pointer, you can call <b>CoMarshalInterface</b> on the object to do so.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imarshal-marshalinterface">IMarshal::MarshalInterface</a>