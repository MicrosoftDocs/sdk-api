---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0003 structure


## -description


This structure contains information about a connection event.


## -struct-fields




### -field userName

The user name.


### -field clientName

The name of the client computer.


### -field authType

A value of the <a href="https://msdn.microsoft.com/ff80f8ac-8378-4087-aa95-a081d2dd710a">AAAuthSchemes</a> enumeration type that specifies the type of authentication used to connect to RD Gateway.


### -field resourceName

The name of the remote computer.


### -field portNumber

The port number of the remote computer used by the connection.


### -field protocolName

The name of the protocol used by the connection.


### -field numberOfBytesReceived

The number of bytes sent from the client to the remote computer.


### -field numberOfBytesTransfered

The number of bytes sent from the remote computer to the client.


### -field reasonForDisconnect

The reason the connection was disconnected.


### -field mainSessionId

A unique identifier assigned to the connection  by RD Gateway.


### -field subSessionId

A unique identifier assigned to the subsession by RD Gateway.

