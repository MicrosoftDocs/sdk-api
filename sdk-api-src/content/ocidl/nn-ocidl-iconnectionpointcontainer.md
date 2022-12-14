---
UID: NN:ocidl.IConnectionPointContainer
title: IConnectionPointContainer (ocidl.h)
description: Supports connection points for connectable objects. (IConnectionPointContainer)
helpviewer_keywords: ["IConnectionPointContainer","IConnectionPointContainer interface [COM]","IConnectionPointContainer interface [COM]","described","_com_iconnectionpointcontainer","com.iconnectionpointcontainer","ocidl/IConnectionPointContainer"]
old-location: com\iconnectionpointcontainer.htm
tech.root: com
ms.assetid: 5e2be055-7baa-4c42-bd20-b338da296ab0
ms.date: 12/05/2018
ms.keywords: IConnectionPointContainer, IConnectionPointContainer interface [COM], IConnectionPointContainer interface [COM],described, _com_iconnectionpointcontainer, com.iconnectionpointcontainer, ocidl/IConnectionPointContainer
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
 - IConnectionPointContainer
 - ocidl/IConnectionPointContainer
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
 - IConnectionPointContainer
---

# IConnectionPointContainer interface


## -description

Supports connection points for connectable objects.

## -inheritance

The <b>IConnectionPointContainer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConnectionPointContainer</b> also has these types of members:

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



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints">IEnumConnectionPoints</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ienumconnections">IEnumConnections</a>
