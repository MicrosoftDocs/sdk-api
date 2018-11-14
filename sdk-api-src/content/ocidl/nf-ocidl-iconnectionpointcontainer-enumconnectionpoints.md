---
UID: NF:ocidl.IConnectionPointContainer.EnumConnectionPoints
title: IConnectionPointContainer::EnumConnectionPoints
author: windows-sdk-content
description: Creates an enumerator object to iterate through all the connection points supported in the connectable object, one connection point per outgoing IID.
old-location: com\iconnectionpointcontainer_enumconnectionpoints.htm
tech.root: com
ms.assetid: 527f94b6-af8e-4ff0-8e99-cd4c5d692628
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EnumConnectionPoints, EnumConnectionPoints method [COM], EnumConnectionPoints method [COM],IConnectionPointContainer interface, IConnectionPointContainer interface [COM],EnumConnectionPoints method, IConnectionPointContainer.EnumConnectionPoints, IConnectionPointContainer::EnumConnectionPoints, _com_iconnectionpointcontainer_enumconnectionpoints, com.iconnectionpointcontainer_enumconnectionpoints, ocidl/IConnectionPointContainer::EnumConnectionPoints
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IConnectionPointContainer.EnumConnectionPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- ocidl.h
: 
- IConnectionPointContainer.EnumConnectionPoints
: 
---

# IConnectionPointContainer::EnumConnectionPoints


## -description


Creates an enumerator object to iterate through all the connection points supported in the connectable object, one connection point per outgoing IID.


## -parameters




### -param ppEnum [out]

A pointer to an <a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a> interface pointer variable that receives the pointer to the newly created enumerator.


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



Because <a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a> enumerates pointers to <a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>, the caller must use <a href="https://msdn.microsoft.com/d97bda43-0d4f-4ae2-b3d8-2c47d25de01a">IConnectionPoint::GetConnectionInterface</a> to determine the interface identifier of the outgoing interface that the connection point supports.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> when the enumerator is no longer needed.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Returning E_NOTIMPL is specifically disallowed because, with the exception of type information, there would be no other means through which a caller could find the IIDs of the outgoing interfaces. Since a connectable object typically has a fixed set of known outgoing interfaces, it is straightforward to implement the enumerator on top of a fixed length array of IIDs known at compile time.





## -see-also




<a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a>



<a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a>
 

 

