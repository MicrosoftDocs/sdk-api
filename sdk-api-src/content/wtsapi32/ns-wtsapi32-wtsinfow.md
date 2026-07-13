---
UID: NS:wtsapi32._WTSINFOW
title: WTSINFOW (wtsapi32.h)
description: Contains information about a Remote Desktop Services session. (WTSINFOW)
helpviewer_keywords: ["*PWTSINFOW","PWTSINFO","PWTSINFO structure pointer [Remote Desktop Services]","WTSINFO","WTSINFO structure [Remote Desktop Services]","WTSINFOA","WTSINFOW","termserv.wtsinfo","wtsapi32/PWTSINFO","wtsapi32/WTSINFO","wtsapi32/WTSINFOA","wtsapi32/WTSINFOW"]
old-location: termserv\wtsinfo.htm
tech.root: TermServ
ms.assetid: 14e2d3bb-8c83-45aa-aa63-87afef3008b3
ms.date: 12/05/2018
ms.keywords: '*PWTSINFOW, PWTSINFO, PWTSINFO structure pointer [Remote Desktop Services], WTSINFO, WTSINFO structure [Remote Desktop Services], WTSINFOA, WTSINFOW, termserv.wtsinfo, wtsapi32/PWTSINFO, wtsapi32/WTSINFO, wtsapi32/WTSINFOA, wtsapi32/WTSINFOW'
req.header: wtsapi32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WTSINFOW (Unicode) and WTSINFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WTSINFOW, *PWTSINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WTSINFOW
 - wtsapi32/_WTSINFOW
 - PWTSINFOW
 - wtsapi32/PWTSINFOW
 - WTSINFOW
 - wtsapi32/WTSINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wtsapi32.h
api_name:
 - WTSINFO
 - WTSINFOA
 - WTSINFOW
---

# WTSINFOW structure


## -description

Contains information about a Remote Desktop Services session.

## -struct-fields

### -field State

A value of the <a href="/windows/desktop/api/wtsapi32/ne-wtsapi32-wts_connectstate_class">WTS_CONNECTSTATE_CLASS</a> enumeration type that indicates the session's current connection state.

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

### -field OutgoingCompressedBytes

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

## -remarks

> [!NOTE]
> The wtsapi32.h header defines WTSINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
