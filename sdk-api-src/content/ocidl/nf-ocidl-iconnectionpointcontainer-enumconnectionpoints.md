---
UID: NF:ocidl.IConnectionPointContainer.EnumConnectionPoints
title: IConnectionPointContainer::EnumConnectionPoints (ocidl.h)
description: Creates an enumerator object to iterate through all the connection points supported in the connectable object, one connection point per outgoing IID.
helpviewer_keywords: ["EnumConnectionPoints","EnumConnectionPoints method [COM]","EnumConnectionPoints method [COM]","IConnectionPointContainer interface","IConnectionPointContainer interface [COM]","EnumConnectionPoints method","IConnectionPointContainer.EnumConnectionPoints","IConnectionPointContainer::EnumConnectionPoints","_com_iconnectionpointcontainer_enumconnectionpoints","com.iconnectionpointcontainer_enumconnectionpoints","ocidl/IConnectionPointContainer::EnumConnectionPoints"]
old-location: com\iconnectionpointcontainer_enumconnectionpoints.htm
tech.root: com
ms.assetid: 527f94b6-af8e-4ff0-8e99-cd4c5d692628
ms.date: 12/05/2018
ms.keywords: EnumConnectionPoints, EnumConnectionPoints method [COM], EnumConnectionPoints method [COM],IConnectionPointContainer interface, IConnectionPointContainer interface [COM],EnumConnectionPoints method, IConnectionPointContainer.EnumConnectionPoints, IConnectionPointContainer::EnumConnectionPoints, _com_iconnectionpointcontainer_enumconnectionpoints, com.iconnectionpointcontainer_enumconnectionpoints, ocidl/IConnectionPointContainer::EnumConnectionPoints
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IConnectionPointContainer::EnumConnectionPoints
 - ocidl/IConnectionPointContainer::EnumConnectionPoints
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IConnectionPointContainer.EnumConnectionPoints
---

# IConnectionPointContainer::EnumConnectionPoints


## -description

Creates an enumerator object to iterate through all the connection points supported in the connectable object, one connection point per outgoing IID.

## -parameters

### -param ppEnum [out]

A pointer to an <a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a> interface pointer variable that receives the pointer to the newly created enumerator.

## -returns

This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The enumerator object was created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppEnum</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Because <a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a> enumerates pointers to <a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>, the caller must use <a href="/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-getconnectioninterface">IConnectionPoint::GetConnectionInterface</a> to determine the interface identifier of the outgoing interface that the connection point supports.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The caller is responsible for calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> when the enumerator is no longer needed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Returning E_NOTIMPL is specifically disallowed because, with the exception of type information, there would be no other means through which a caller could find the IIDs of the outgoing interfaces. Since a connectable object typically has a fixed set of known outgoing interfaces, it is straightforward to implement the enumerator on top of a fixed length array of IIDs known at compile time.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>