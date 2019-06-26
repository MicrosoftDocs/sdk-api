---
UID: NN:ocidl.IConnectionPoint
title: IConnectionPoint (ocidl.h)
author: windows-sdk-content
description: Supports connection points for connectable objects.
old-location: com\iconnectionpoint.htm
tech.root: com
ms.assetid: ef5a917c-b57f-4000-8daa-86fdbfb47579
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConnectionPoint, IConnectionPoint interface [COM], IConnectionPoint interface [COM],described, _com_iconnectionpoint, com.iconnectionpoint, ocidl/IConnectionPoint
ms.topic: interface
f1_keywords: 
 - "ocidl/IConnectionPoint"
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
 - IConnectionPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConnectionPoint interface


## -description


Supports connection points for connectable objects.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectionPoint</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConnectionPoint</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-advise">Advise</a>
</td>
<td align="left" width="63%">
Establishes a connection between a connection point object and a client's sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-enumconnections">EnumConnections</a>
</td>
<td align="left" width="63%">
Creates an enumerator object to iterate through the current connections for this connection point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-getconnectioninterface">GetConnectionInterface</a>
</td>
<td align="left" width="63%">
Retrieves the IID of the outgoing interface managed by this connection point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer">GetConnectionPointContainer</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> interface pointer for the parent connectable object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpoint-unadvise">Unadvise</a>
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




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
 

 

