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

# _WTSINFOW structure


## -description


Contains information about a Remote Desktop Services session.


## -struct-fields




### -field State

A value of the <a href="https://msdn.microsoft.com/ee376f5a-3474-4e31-94c1-e760346eb794">WTS_CONNECTSTATE_CLASS</a> enumeration type that indicates the session's current connection state.


### -field SessionId

The session identifier.


### -field IncomingBytes

Uncompressed Remote Desktop Protocol (RDP) data from the client to the server.


### -field OutgoingBytes

Uncompressed RDP data from the server to the client.


### -field IncomingFrames

The number of frames of RDP data sent from the client to the server since the client connected.


### -field OutgoingFrames

The number of frames of RDP data sent from the server to the client since the client connected.


### -field IncomingCompressedBytes

Compressed RDP data from the client to the server.


#### - OutgoingCompressedBytes

Compressed RDP data from the server to the client.


### -field WinStationName

A null-terminated string that contains the name of the WinStation for the session.


### -field Domain

A null-terminated string that contains the name of the domain that the user belongs to.


### -field UserName

A null-terminated string that contains the name of the user who owns the session.


### -field ConnectTime

The most recent client connection time.


### -field DisconnectTime

The last client disconnection time.


### -field LastInputTime

The time of the last user input in the session.


### -field LogonTime

The time that the user logged on to the session.


### -field CurrentTime

The time that the <b>WTSINFO</b> data structure was called.

