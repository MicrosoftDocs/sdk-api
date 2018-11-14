---
UID: NN:ocidl.IConnectionPointContainer
title: IConnectionPointContainer
author: windows-sdk-content
description: Supports connection points for connectable objects.
old-location: com\iconnectionpointcontainer.htm
tech.root: com
ms.assetid: 5e2be055-7baa-4c42-bd20-b338da296ab0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IConnectionPointContainer, IConnectionPointContainer interface [COM], IConnectionPointContainer interface [COM],described, _com_iconnectionpointcontainer, com.iconnectionpointcontainer, ocidl/IConnectionPointContainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IConnectionPointContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConnectionPointContainer interface


## -description


Supports connection points for connectable objects.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectionPointContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IConnectionPointContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConnectionPointContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/527f94b6-af8e-4ff0-8e99-cd4c5d692628">EnumConnectionPoints</a>
</td>
<td align="left" width="63%">
Creates an enumerator object to iterate through all the connection points supported in the connectable object, one connection point per outgoing IID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbe55013-13ca-43e8-8d5e-ef89076df039">FindConnectionPoint</a>
</td>
<td align="left" width="63%">
Returns a pointer to the <a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a> interface of a connection point for a specified IID, if that IID describes a supported outgoing interface.

</td>
</tr>
</table> 


## -remarks



Connectable objects support the following features: 



<ul>
<li>Outgoing interfaces, such as event sets
</li>
<li>The ability to enumerate the IIDs of the outgoing interfaces
</li>
<li>The ability to connect and disconnect sinks to the object for those outgoing IIDs
</li>
<li>The ability to enumerate the connections that exist to a particular outgoing interface
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ef5a917c-b57f-4000-8daa-86fdbfb47579">IConnectionPoint</a>



<a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a>



<a href="https://msdn.microsoft.com/464966c1-e4e9-4b58-9e41-48de408f572f">IEnumConnections</a>
 

 

