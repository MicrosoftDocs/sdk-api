---
UID: NF:ocidl.IConnectionPoint.EnumConnections
title: IConnectionPoint::EnumConnections
author: windows-sdk-content
description: Creates an enumerator object to iterate through the current connections for this connection point.
old-location: com\iconnectionpoint_enumconnections.htm
old-project: com
ms.assetid: 424aab99-990e-4b45-9b58-ac22b2cee87c
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: EnumConnections, EnumConnections method [COM], EnumConnections method [COM],IConnectionPoint interface, IConnectionPoint interface [COM],EnumConnections method, IConnectionPoint.EnumConnections, IConnectionPoint::EnumConnections, _com_iconnectionpoint_enumconnections, com.iconnectionpoint_enumconnections, ocidl/IConnectionPoint::EnumConnections
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IConnectionPoint.EnumConnections
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IConnectionPoint::EnumConnections


## -description


Creates an enumerator object to iterate through the current connections for this connection point.


## -parameters




### -param ppEnum [out]

A pointer to an <a href="https://msdn.microsoft.com/464966c1-e4e9-4b58-9e41-48de408f572f">IEnumConnections</a> interface pointer that receives the newly created enumerator.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The connection point does not support enumeration.

</td>
</tr>
</table>
 




## -remarks



The caller is responsible for calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> when the enumerator is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>



<a href="https://msdn.microsoft.com/464966c1-e4e9-4b58-9e41-48de408f572f">IEnumConnections</a>
 

 

