---
UID: NF:ocidl.IConnectionPoint.GetConnectionPointContainer
title: IConnectionPoint::GetConnectionPointContainer
author: windows-sdk-content
description: Retrieves the IConnectionPointContainer interface pointer for the parent connectable object.
old-location: com\iconnectionpoint_getconnectionpointcontainer.htm
tech.root: com
ms.assetid: 12c0c777-27ce-4e6d-8e9a-f6333e4112bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetConnectionPointContainer, GetConnectionPointContainer method [COM], GetConnectionPointContainer method [COM],IConnectionPoint interface, IConnectionPoint interface [COM],GetConnectionPointContainer method, IConnectionPoint.GetConnectionPointContainer, IConnectionPoint::GetConnectionPointContainer, _com_iconnectionpoint_getconnectionpointcontainer, com.iconnectionpoint_getconnectionpointcontainer, ocidl/IConnectionPoint::GetConnectionPointContainer
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
 - IConnectionPoint.GetConnectionPointContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConnectionPoint::GetConnectionPointContainer


## -description


Retrieves the <a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a> interface pointer for the parent connectable object.


## -parameters




### -param ppCPC [out]

A pointer to an <a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a> interface pointer.


## -returns



This method can return the standard return value E_UNEXPECTED, as well as the following values.

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
The <a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a> pointer was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>ppCPC</i> is not a valid interface pointer. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a>. The caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> to release this pointer when done.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> before returning.

This method must be implemented in any connection point; E_NOTIMPL is not an acceptable return value.




## -see-also




<a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>



<a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a>
 

 

