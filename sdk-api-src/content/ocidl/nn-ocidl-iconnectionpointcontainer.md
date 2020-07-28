---
UID: NN:ocidl.IConnectionPointContainer
title: IConnectionPointContainer (ocidl.h)
description: Supports connection points for connectable objects.
helpviewer_keywords: ["IConnectionPointContainer","IConnectionPointContainer interface [COM]","IConnectionPointContainer interface [COM]","described","_com_iconnectionpointcontainer","com.iconnectionpointcontainer","ocidl/IConnectionPointContainer"]
old-location: com\iconnectionpointcontainer.htm
tech.root: com
ms.assetid: 5e2be055-7baa-4c42-bd20-b338da296ab0
ms.date: 12/05/2018
ms.keywords: IConnectionPointContainer, IConnectionPointContainer interface [COM], IConnectionPointContainer interface [COM],described, _com_iconnectionpointcontainer, com.iconnectionpointcontainer, ocidl/IConnectionPointContainer
f1_keywords:
- ocidl/IConnectionPointContainer
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConnectionPointContainer interface


## -description


Supports connection points for connectable objects.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConnectionPointContainer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConnectionPointContainer</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints">EnumConnectionPoints</a>
</td>
<td align="left" width="63%">
Creates an enumerator object to iterate through all the connection points supported in the connectable object, one connection point per outgoing IID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint">FindConnectionPoint</a>
</td>
<td align="left" width="63%">
Returns a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface of a connection point for a specified IID, if that IID describes a supported outgoing interface.

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




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
 

 

