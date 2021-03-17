---
UID: NF:sbtsv.ITsSbClientConnection.get_ClientConnectionPropertySet
title: ITsSbClientConnection::get_ClientConnectionPropertySet (sbtsv.h)
description: Retrieves an object that contains properties associated with the client connection.
helpviewer_keywords: ["ClientConnectionPropertySet property [Remote Desktop Services]","ClientConnectionPropertySet property [Remote Desktop Services]","ITsSbClientConnection interface","ITsSbClientConnection interface [Remote Desktop Services]","ClientConnectionPropertySet property","ITsSbClientConnection.ClientConnectionPropertySet","ITsSbClientConnection.get_ClientConnectionPropertySet","ITsSbClientConnection::ClientConnectionPropertySet","ITsSbClientConnection::get_ClientConnectionPropertySet","get_ClientConnectionPropertySet","sbtsv/ITsSbClientConnection::ClientConnectionPropertySet","sbtsv/ITsSbClientConnection::get_ClientConnectionPropertySet","termserv.itssbclientconnection_clientconnectionpropertyset"]
old-location: termserv\itssbclientconnection_clientconnectionpropertyset.htm
tech.root: TermServ
ms.assetid: 488c5b71-7139-4744-93bf-484d05457d0f
ms.date: 12/05/2018
ms.keywords: ClientConnectionPropertySet property [Remote Desktop Services], ClientConnectionPropertySet property [Remote Desktop Services],ITsSbClientConnection interface, ITsSbClientConnection interface [Remote Desktop Services],ClientConnectionPropertySet property, ITsSbClientConnection.ClientConnectionPropertySet, ITsSbClientConnection.get_ClientConnectionPropertySet, ITsSbClientConnection::ClientConnectionPropertySet, ITsSbClientConnection::get_ClientConnectionPropertySet, get_ClientConnectionPropertySet, sbtsv/ITsSbClientConnection::ClientConnectionPropertySet, sbtsv/ITsSbClientConnection::get_ClientConnectionPropertySet, termserv.itssbclientconnection_clientconnectionpropertyset
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
 - ITsSbClientConnection::get_ClientConnectionPropertySet
 - sbtsv/ITsSbClientConnection::get_ClientConnectionPropertySet
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
 - ITsSbClientConnection.ClientConnectionPropertySet
 - ITsSbClientConnection.get_ClientConnectionPropertySet
---

# ITsSbClientConnection::get_ClientConnectionPropertySet


## -description

Retrieves an object that contains properties associated with the client connection.

This property is read-only.

## -parameters

## -remarks

Plug-ins can use this interface to store custom properties for the lifetime of a connection request.


By default, Remote Desktop Connection Broker (RD Connection Broker) sets the following properties for the property set object.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection">ITsSbClientConnection</a>