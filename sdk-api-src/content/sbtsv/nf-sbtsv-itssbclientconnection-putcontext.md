---
UID: NF:sbtsv.ITsSbClientConnection.PutContext
title: ITsSbClientConnection::PutContext (sbtsv.h)
description: Can be used by plug-ins to store context information specific to the connection.
helpviewer_keywords: ["ITsSbClientConnection interface [Remote Desktop Services]","PutContext method","ITsSbClientConnection.PutContext","ITsSbClientConnection::PutContext","PutContext","PutContext method [Remote Desktop Services]","PutContext method [Remote Desktop Services]","ITsSbClientConnection interface","sbtsv/ITsSbClientConnection::PutContext","termserv.itssbclientconnection_putcontext"]
old-location: termserv\itssbclientconnection_putcontext.htm
tech.root: TermServ
ms.assetid: 654714ef-cc86-41e8-8759-bbb66bd61cd2
ms.date: 12/05/2018
ms.keywords: ITsSbClientConnection interface [Remote Desktop Services],PutContext method, ITsSbClientConnection.PutContext, ITsSbClientConnection::PutContext, PutContext, PutContext method [Remote Desktop Services], PutContext method [Remote Desktop Services],ITsSbClientConnection interface, sbtsv/ITsSbClientConnection::PutContext, termserv.itssbclientconnection_putcontext
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
 - ITsSbClientConnection::PutContext
 - sbtsv/ITsSbClientConnection::PutContext
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
 - ITsSbClientConnection.PutContext
---

# ITsSbClientConnection::PutContext


## -description

Can be used by plug-ins to store context information specific to the connection.

## -parameters

### -param contextId [in]

A <b>BSTR</b> variable that contains the context ID. We recommend using unique identifiers as context IDs to avoid collisions between plug-ins. A client connection object can be used by more than one plug-in.

### -param context [in]

The context information to store.

### -param existingContext [out, optional]

Existing context information for the supplied context ID, if any, is returned in this parameter. The existing information is overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Plug-ins can use the client connection object to store context information that is specific to a connection request. This allows plug-ins to remain stateless and rely exclusively on state information stored by connection requests. Plug-ins that use this method can also register for connection request notifications. Contexts can be deleted upon receipt of CONNECTION_REQUEST_FAILED, CONNECTION_REQUEST_TIMEDOUT, or CONNECTION_REQUEST_SUCCEEDED notifications. These notifications indicate that the connection request is about to be deleted.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>