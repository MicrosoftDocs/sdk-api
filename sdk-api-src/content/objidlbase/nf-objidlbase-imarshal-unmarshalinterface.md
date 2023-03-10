---
UID: NF:objidlbase.IMarshal.UnmarshalInterface
title: IMarshal::UnmarshalInterface (objidlbase.h)
description: The IMarshal::UnmarshalInterface (objidlbase.h) method unmarshals an interface pointer.
helpviewer_keywords: ["IMarshal interface [COM]","UnmarshalInterface method","IMarshal.UnmarshalInterface","IMarshal::UnmarshalInterface","UnmarshalInterface","UnmarshalInterface method [COM]","UnmarshalInterface method [COM]","IMarshal interface","_com_imarshal_unmarshalinterface","com.imarshal_unmarshalinterface","objidlbase/IMarshal::UnmarshalInterface"]
old-location: com\imarshal_unmarshalinterface.htm
tech.root: com
ms.assetid: 5b496028-57db-447e-8c5c-76b7ea0fa4ee
ms.date: 08/13/2022
ms.keywords: IMarshal interface [COM],UnmarshalInterface method, IMarshal.UnmarshalInterface, IMarshal::UnmarshalInterface, UnmarshalInterface, UnmarshalInterface method [COM], UnmarshalInterface method [COM],IMarshal interface, _com_imarshal_unmarshalinterface, com.imarshal_unmarshalinterface, objidlbase/IMarshal::UnmarshalInterface
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMarshal::UnmarshalInterface
 - objidlbase/IMarshal::UnmarshalInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IMarshal.UnmarshalInterface
---

# IMarshal::UnmarshalInterface


## -description

Unmarshals an interface pointer.

## -parameters

### -param pStm [in]

A pointer to the stream from which the interface pointer is to be unmarshaled.

### -param riid [in]

A reference to the identifier of the interface to be unmarshaled.

### -param ppv [out]

The address of pointer variable that receives the interface pointer. Upon successful return, *<i>ppv</i> contains the requested interface pointer of the interface to be unmarshaled.

## -returns

This method can return the standard return value E_FAIL, as well as the following values.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The specified interface is not supported.

</td>
</tr>
</table>

## -remarks

The COM library in the process where unmarshaling is to occur calls the proxy's implementation of this method.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
You do not call this method directly. There are, however, some situations in which you might call it indirectly through a call to <a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>. For example, if you are implementing a stub, your implementation would call <b>CoUnmarshalInterface</b> when the stub receives an interface pointer as a parameter in a method call.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The proxy's implementation should read the data written to the stream by the original object's implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-marshalinterface">IMarshal::MarshalInterface</a> and use that data to initialize the proxy object whose CLSID was returned by the marshaling stub's call to the original object's implementation of <a href="/windows/desktop/api/objidl/nf-objidl-imarshal-getunmarshalclass">IMarshal::GetUnmarshalClass</a>.

To return the appropriate interface pointer, the proxy implementation can simply call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on itself, passing the <i>riid</i> and <i>ppv</i> parameters. However, your implementation of <b>UnmarshalInterface</b> is free to create a different object and, if necessary, return a pointer to it.

Just before exiting, even if exiting with an error, your implementation should reposition the seek pointer in the stream immediately after the last byte of data read.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface">CoUnmarshalInterface</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshal">IMarshal</a>
