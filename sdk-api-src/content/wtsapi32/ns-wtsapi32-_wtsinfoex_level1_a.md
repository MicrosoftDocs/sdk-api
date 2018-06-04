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

# _WTSINFOEX_LEVEL1_A structure


## -description


Contains extended information about  a Remote Desktop Services session.


## -struct-fields




### -field SessionId

The session identifier.


### -field SessionState

A value of the <a href="https://msdn.microsoft.com/ee376f5a-3474-4e31-94c1-e760346eb794">WTS_CONNECTSTATE_CLASS</a> enumeration type that specifies the connection state of a Remote Desktop Services session.


### -field SessionFlags

The state of the session. This can be one or more of the following values.



#### WTS_SESSIONSTATE_UNKNOWN (4294967295 (0xFFFFFFFF))

The session state is not known.



#### WTS_SESSIONSTATE_LOCK (0 (0x0))

The session is locked.



#### WTS_SESSIONSTATE_UNLOCK (1 (0x1))

The session is unlocked.

<b>Windows Server 2008 R2 and Windows 7:  </b>Due to a code defect, the usage of the <b>WTS_SESSIONSTATE_LOCK</b> and <b>WTS_SESSIONSTATE_UNLOCK</b> flags is reversed. That is, <b>WTS_SESSIONSTATE_LOCK</b> indicates that the session is unlocked, and <b>WTS_SESSIONSTATE_UNLOCK</b> indicates the session is locked.


### -field WinStationName

A  null-terminated string that contains the name of the window station for the session.


### -field UserName

A  null-terminated string that contains the name of the user who owns the session.


### -field DomainName

A  null-terminated string that contains the name of the domain that the user belongs to.


### -field LogonTime

The time that the user logged on to the session.  This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 Coordinated Universal Time (Greenwich Mean Time).


### -field ConnectTime

The time of the most recent client connection to the session. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 Coordinated Universal Time.


### -field DisconnectTime

The time of the most recent client disconnection to the session. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 Coordinated Universal Time.


### -field LastInputTime

The time of the last user input in the session.  This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 Coordinated Universal Time.


### -field CurrentTime

The time that this structure was filled. This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 Coordinated Universal Time.


### -field IncomingBytes

The number of bytes of uncompressed Remote Desktop Protocol (RDP) data sent from the client to the server since the client connected.


### -field OutgoingBytes

The number of bytes of uncompressed RDP data sent from the server to the client since the client connected.


### -field IncomingFrames

The number of frames of RDP data sent from the client to the server since the client connected.


### -field OutgoingFrames

The number of frames of RDP data sent from the server to the client since the client connected.


### -field IncomingCompressedBytes

The number of bytes of compressed RDP data sent from the client to the server since the client connected.


### -field OutgoingCompressedBytes

The number of bytes of compressed RDP data sent from the server to the client since the client connected.


## -see-also




<a href="https://msdn.microsoft.com/ee376f5a-3474-4e31-94c1-e760346eb794">WTS_CONNECTSTATE_CLASS</a>
 

 

