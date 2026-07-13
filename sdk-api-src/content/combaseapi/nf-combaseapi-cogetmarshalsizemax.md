---
UID: NF:combaseapi.CoGetMarshalSizeMax
title: CoGetMarshalSizeMax function (combaseapi.h)
description: Returns an upper bound on the number of bytes needed to marshal the specified interface pointer to the specified object.
helpviewer_keywords: ["CoGetMarshalSizeMax","CoGetMarshalSizeMax function [COM]","_com_CoGetMarshalSizeMax","com.cogetmarshalsizemax","combaseapi/CoGetMarshalSizeMax"]
old-location: com\cogetmarshalsizemax.htm
tech.root: com
ms.assetid: c04c736c-8efe-438b-9d21-8b6ad53d36e7
ms.date: 12/05/2018
ms.keywords: CoGetMarshalSizeMax, CoGetMarshalSizeMax function [COM], _com_CoGetMarshalSizeMax, com.cogetmarshalsizemax, combaseapi/CoGetMarshalSizeMax
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
 - CoGetMarshalSizeMax
 - combaseapi/CoGetMarshalSizeMax
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
 - CoGetMarshalSizeMax
---

# CoGetMarshalSizeMax function


## -description

Returns an upper bound on the number of bytes needed to marshal the specified interface pointer to the specified object.

## -parameters

### -param pulSize [out]

A pointer to the upper-bound value on the size, in bytes, of the data packet to be written to the marshaling stream. If this parameter is 0, the size of the packet is unknown.

### -param riid [in]

A reference to the identifier of the interface whose pointer is to be marshaled. This interface must be derived from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param pUnk [in]

A pointer to the interface to be marshaled. This interface must be derived from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

### -param dwDestContext [in]

The destination context where the specified interface is to be unmarshaled. Values for <i>dwDestContext</i> come from the enumeration <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshctx">MSHCTX</a>.

### -param pvDestContext [in, optional]

This parameter is reserved and must be <b>NULL</b>.

### -param mshlflags [in]

Indicates whether the data to be marshaled is to be transmitted back to the client process the normal case or written to a global table, where it can be retrieved by multiple clients. Values come from the enumeration <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-mshlflags">MSHLFLAGS</a>.

## -returns

This function can return the standard return value E_UNEXPECTED, as well as the following values.

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
The upper bound was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
Before this function can be called, either the <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a> or <a href="/windows/desktop/api/ole2/nf-ole2-oleinitialize">OleInitialize</a> function must be called.

</td>
</tr>
</table>

## -remarks

This function performs the following tasks:

<ol>
<li>Queries the object for an <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a> pointer or, if the object does not implement <b>IMarshal</b>, gets a pointer to COM's standard marshaler.
</li>
<li>Using the pointer obtained in the preceding item, calls <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-getmarshalsizemax">IMarshal::GetMarshalSizeMax</a>.
</li>
<li>Adds to the value returned by the call to <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-getmarshalsizemax">GetMarshalSizeMax</a> the size of the marshaling data header and, possibly, that of the proxy CLSID to obtain the maximum size in bytes of the amount of data to be written to the marshaling stream.</li>
</ol>
You do not explicitly call this function unless you are implementing <a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>, in which case your marshaling stub should call this function to get the correct size of the data packet to be marshaled.



The value returned by this method is guaranteed to be valid only as long as the internal state of the object being marshaled does not change. Therefore, the actual marshaling should be done immediately after this function returns, or the stub runs the risk that the object, because of some change in state, might require more memory to marshal than it originally indicated.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface">CoMarshalInterface</a>



<a href="/windows/desktop/api/objidl/nf-objidl-imarshal-getmarshalsizemax">IMarshal::GetMarshalSizeMax</a>