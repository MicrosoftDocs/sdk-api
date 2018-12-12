---
UID: NS:wtsapi32._WTSINFOEX_LEVEL1_A
title: WTSINFOEX_LEVEL1_A
author: windows-sdk-content
description: Contains extended information about a Remote Desktop Services session.
old-location: termserv\wtsinfoex_level1.htm
tech.root: termserv
ms.assetid: bad4f35a-04a9-42fa-b87e-0f51e9f0f30e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PWTSINFOEX_LEVEL1_A, PWTSINFOEX_LEVEL1, PWTSINFOEX_LEVEL1 structure pointer [Remote Desktop Services], WTSINFOEX_LEVEL1, WTSINFOEX_LEVEL1 structure [Remote Desktop Services], WTSINFOEX_LEVEL1_A, WTSINFOEX_LEVEL1_W, WTS_SESSIONSTATE_LOCK, WTS_SESSIONSTATE_UNKNOWN, WTS_SESSIONSTATE_UNLOCK, termserv.wtsinfoex_level1, wtsapi32/PWTSINFOEX_LEVEL1, wtsapi32/WTSINFOEX_LEVEL1, wtsapi32/WTSINFOEX_LEVEL1_A, wtsapi32/WTSINFOEX_LEVEL1_W"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSINFOEX_LEVEL1_W (Unicode) and WTSINFOEX_LEVEL1_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTSINFOEX_LEVEL1
 - WTSINFOEX_LEVEL1_A
 - WTSINFOEX_LEVEL1_W
product: Windows
targetos: Windows
req.typenames: WTSINFOEX_LEVEL1_A, *PWTSINFOEX_LEVEL1_A
req.redist: 
---

# WTSINFOEX_LEVEL1_A structure


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
 

 

