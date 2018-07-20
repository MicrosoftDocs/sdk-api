---
UID: NN:ocidl.IConnectionPoint
title: IConnectionPoint
author: windows-sdk-content
description: Supports connection points for connectable objects.
old-location: com\iconnectionpoint.htm
old-project: com
ms.assetid: ef5a917c-b57f-4000-8daa-86fdbfb47579
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IConnectionPoint, IConnectionPoint interface [COM], IConnectionPoint interface [COM],described, _com_iconnectionpoint, com.iconnectionpoint, ocidl/IConnectionPoint
ms.prod: windows
ms.technology: windows-sdk
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
 - IConnectionPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IConnectionPoint interface


## -description


Supports connection points for connectable objects.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectionPoint</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IConnectionPoint</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConnectionPoint</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11257f24-096c-4240-8fac-4e42a6161d66">Advise</a>
</td>
<td align="left" width="63%">
Establishes a connection between a connection point object and a client's sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/424aab99-990e-4b45-9b58-ac22b2cee87c">EnumConnections</a>
</td>
<td align="left" width="63%">
Creates an enumerator object to iterate through the current connections for this connection point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d97bda43-0d4f-4ae2-b3d8-2c47d25de01a">GetConnectionInterface</a>
</td>
<td align="left" width="63%">
Retrieves the IID of the outgoing interface managed by this connection point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12c0c777-27ce-4e6d-8e9a-f6333e4112bf">GetConnectionPointContainer</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a> interface pointer for the parent connectable object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71641bad-2fd1-4d94-a6d0-116f5687a95b">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection previously established between a connection point object and a client's sink.

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




<a href="https://msdn.microsoft.com/5e2be055-7baa-4c42-bd20-b338da296ab0">IConnectionPointContainer</a>



<a href="https://msdn.microsoft.com/893090f1-a0b4-46f1-a5d0-1da704ca7aa9">IEnumConnectionPoints</a>



<a href="https://msdn.microsoft.com/464966c1-e4e9-4b58-9e41-48de408f572f">IEnumConnections</a>
 

 

