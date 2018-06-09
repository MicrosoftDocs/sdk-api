---
UID: NF:sbtsv.ITsSbClientConnection.get_ClientConnectionPropertySet
title: ITsSbClientConnection::get_ClientConnectionPropertySet
author: windows-sdk-content
description: Retrieves an object that contains properties associated with the client connection.
old-location: termserv\itssbclientconnection_clientconnectionpropertyset.htm
old-project: TermServ
ms.assetid: 488c5b71-7139-4744-93bf-484d05457d0f
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ClientConnectionPropertySet property [Remote Desktop Services], ClientConnectionPropertySet property [Remote Desktop Services],ITsSbClientConnection interface, ITsSbClientConnection interface [Remote Desktop Services],ClientConnectionPropertySet property, ITsSbClientConnection.ClientConnectionPropertySet, ITsSbClientConnection.get_ClientConnectionPropertySet, ITsSbClientConnection::ClientConnectionPropertySet, ITsSbClientConnection::get_ClientConnectionPropertySet, get_ClientConnectionPropertySet, sbtsv/ITsSbClientConnection::ClientConnectionPropertySet, sbtsv/ITsSbClientConnection::get_ClientConnectionPropertySet, termserv.itssbclientconnection_clientconnectionpropertyset
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TS_SB_SORT_BY
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>
 

 

