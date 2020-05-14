---
UID: NN:ocidl.IEnumConnections
title: IEnumConnections (ocidl.h)
description: Enumerates the current connections for a connectable object.helpviewer_keywords: ["IEnumConnections","IEnumConnections interface [COM]","IEnumConnections interface [COM]","described","_com_ienumconnections","com.ienumconnections","ocidl/IEnumConnections"]
old-location: com\ienumconnections.htm
tech.root: com
ms.assetid: 464966c1-e4e9-4b58-9e41-48de408f572f
ms.date: 12/05/2018
ms.keywords: IEnumConnections, IEnumConnections interface [COM], IEnumConnections interface [COM],described, _com_ienumconnections, com.ienumconnections, ocidl/IEnumConnections
f1_keywords:
- ocidl/IEnumConnections
dev_langs:
- c++
req.header: ocidl.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ocidl.h
api_name:
- IEnumConnections
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumConnections interface


## -description


Enumerates the current connections for a connectable object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumConnections</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumConnections</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumConnections</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ienumconnections-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ienumconnections-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ienumconnections-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ienumconnections-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

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



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>
 

 

