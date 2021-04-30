---
UID: NS:wsnwlink._IPX_SPXCONNSTATUS_DATA
title: IPX_SPXCONNSTATUS_DATA (wsnwlink.h)
description: The IPX_SPXCONNSTATUS_DATA structure provides information about a connected SPX socket.
helpviewer_keywords: ["*PIPX_SPXCONNSTATUS_DATA","IPX_SPXCONNSTATUS_DATA","IPX_SPXCONNSTATUS_DATA structure [Winsock]","PIPX_SPXCONNSTATUS_DATA","PIPX_SPXCONNSTATUS_DATA structure pointer [Winsock]","_win32_ipx_spxconnstatus_data_2","winsock.ipx_spxconnstatus_data_2","wsnwlink/IPX_SPXCONNSTATUS_DATA","wsnwlink/PIPX_SPXCONNSTATUS_DATA"]
old-location: winsock\ipx_spxconnstatus_data_2.htm
tech.root: WinSock
ms.assetid: 741fdb22-a92c-4159-bde6-e3d18a222b9e
ms.date: 12/05/2018
ms.keywords: '*PIPX_SPXCONNSTATUS_DATA, IPX_SPXCONNSTATUS_DATA, IPX_SPXCONNSTATUS_DATA structure [Winsock], PIPX_SPXCONNSTATUS_DATA, PIPX_SPXCONNSTATUS_DATA structure pointer [Winsock], _win32_ipx_spxconnstatus_data_2, winsock.ipx_spxconnstatus_data_2, wsnwlink/IPX_SPXCONNSTATUS_DATA, wsnwlink/PIPX_SPXCONNSTATUS_DATA'
req.header: wsnwlink.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPX_SPXCONNSTATUS_DATA, *PIPX_SPXCONNSTATUS_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IPX_SPXCONNSTATUS_DATA
 - wsnwlink/_IPX_SPXCONNSTATUS_DATA
 - PIPX_SPXCONNSTATUS_DATA
 - wsnwlink/PIPX_SPXCONNSTATUS_DATA
 - IPX_SPXCONNSTATUS_DATA
 - wsnwlink/IPX_SPXCONNSTATUS_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsnwlink.h
api_name:
 - IPX_SPXCONNSTATUS_DATA
---

# IPX_SPXCONNSTATUS_DATA structure


## -description

The 
<b>IPX_SPXCONNSTATUS_DATA</b> structure provides information about a connected SPX socket. Used in conjunction with 
<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a> function calls that specify IPX_SPXGETCONNECTIONSTATUS in the <i>optname</i> parameter. All numbers in 
<b>IPX_SPXCONNSTATUS_DATA</b> are in Novell (high-low) order.

## -struct-fields

### -field ConnectionState

Specifies the connection state.

### -field WatchDogActive

Specifies whether watchdog capabilities are active.

### -field LocalConnectionId

Specifies the local connection ID.

### -field RemoteConnectionId

Specifies the remote connection ID.

### -field LocalSequenceNumber

Specifies the local sequence number.

### -field LocalAckNumber

Specifies the local acknowledgment (ACK) number.

### -field LocalAllocNumber

Specifies the local allocation number.

### -field RemoteAckNumber

Specifies the remote acknowledgment (ACK) number.

### -field RemoteAllocNumber

Specifies the remote allocation number.

### -field LocalSocket

Specifies the local socket.

### -field ImmediateAddress

Specifies the IPX address to which the local computer is attached.

### -field RemoteNetwork

Specifies the network to which the remote host is attached.

### -field RemoteNode

Specifies the remote node.

### -field RemoteSocket

Specifies the remote socket.

### -field RetransmissionCount

Specifies the number of retransmissions.

### -field EstimatedRoundTripDelay

Specifies the estimated round trip–time, in milliseconds, delay for a given packet.

### -field RetransmittedPackets

Specifies the number of retransmitted packets on the socket.

### -field SuppressedPacket

Specifies the number of suppressed packets on the socket.

## -see-also

<a href="/windows/desktop/api/winsock/nf-winsock-getsockopt">getsockopt</a>