---
UID: NN:ocidl.IConnectionPoint
title: IConnectionPoint (ocidl.h)
description: Supports connection points for connectable objects. (IConnectionPoint)
helpviewer_keywords: ["IConnectionPoint","IConnectionPoint interface [COM]","IConnectionPoint interface [COM]","described","_com_iconnectionpoint","com.iconnectionpoint","ocidl/IConnectionPoint"]
old-location: com\iconnectionpoint.htm
tech.root: com
ms.assetid: ef5a917c-b57f-4000-8daa-86fdbfb47579
ms.date: 12/05/2018
ms.keywords: IConnectionPoint, IConnectionPoint interface [COM], IConnectionPoint interface [COM],described, _com_iconnectionpoint, com.iconnectionpoint, ocidl/IConnectionPoint
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
 - IConnectionPoint
 - ocidl/IConnectionPoint
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
 - IConnectionPoint
---

# IConnectionPoint interface


## -description

Supports connection points for connectable objects.

## -inheritance

The <b>IConnectionPoint</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConnectionPoint</b> also has these types of members:

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

<a href="/windows/desktop/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
