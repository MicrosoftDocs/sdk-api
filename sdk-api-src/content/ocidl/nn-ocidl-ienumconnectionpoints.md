---
UID: NN:ocidl.IEnumConnectionPoints
title: IEnumConnectionPoints (ocidl.h)
description: Enumerates connection points.
helpviewer_keywords: ["IEnumConnectionPoints","IEnumConnectionPoints interface [COM]","IEnumConnectionPoints interface [COM]","described","_com_ienumconnectionpoints","com.ienumconnectionpoints","ocidl/IEnumConnectionPoints"]
old-location: com\ienumconnectionpoints.htm
tech.root: com
ms.assetid: 893090f1-a0b4-46f1-a5d0-1da704ca7aa9
ms.date: 12/05/2018
ms.keywords: IEnumConnectionPoints, IEnumConnectionPoints interface [COM], IEnumConnectionPoints interface [COM],described, _com_ienumconnectionpoints, com.ienumconnectionpoints, ocidl/IEnumConnectionPoints
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumConnectionPoints
 - ocidl/IEnumConnectionPoints
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ocidl.h
api_name:
 - IEnumConnectionPoints
---

# IEnumConnectionPoints interface


## -description

 Enumerates connection points.

## -inheritance

The <b>IEnumConnectionPoints</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumConnectionPoints</b> also has these types of members:

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

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
