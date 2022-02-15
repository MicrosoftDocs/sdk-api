---
UID: NN:sbtsv.ITsSbClientConnection
title: ITsSbClientConnection (sbtsv.h)
description: Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.
helpviewer_keywords: ["ITsSbClientConnection","ITsSbClientConnection interface [Remote Desktop Services]","ITsSbClientConnection interface [Remote Desktop Services]","described","sbtsv/ITsSbClientConnection","termserv.itssbclientconnection"]
old-location: termserv\itssbclientconnection.htm
tech.root: TermServ
ms.assetid: 6649f43d-0e2a-42d7-8111-862bb28e3dbc
ms.date: 12/05/2018
ms.keywords: ITsSbClientConnection, ITsSbClientConnection interface [Remote Desktop Services], ITsSbClientConnection interface [Remote Desktop Services],described, sbtsv/ITsSbClientConnection, termserv.itssbclientconnection
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbClientConnection
 - sbtsv/ITsSbClientConnection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbClientConnection
---

# ITsSbClientConnection interface


## -description

Exposes methods and properties that store state information about an incoming connection request from a 
    Remote Desktop  Connection (RDC) client. This information does not need to be stored on the resource or 
    filter plug-ins, which allows the plug-ins to be stateless.

Plug-ins can use this interface to obtain information about a connection request initiated by a client, and then 
    make decisions about load balancing, placement, and orchestration. This interface also stores the results of all 
    these operations. A <b>ITsSbClientConnection</b> object 
    should persist until the client successfully logs on to a target computer.

## -inheritance

The <b>ITsSbClientConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbClientConnection</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
