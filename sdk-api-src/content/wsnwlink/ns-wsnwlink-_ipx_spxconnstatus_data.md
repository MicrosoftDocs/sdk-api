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

# _IPX_SPXCONNSTATUS_DATA structure


## -description



			The 
<b>IPX_SPXCONNSTATUS_DATA</b> structure provides information about a connected SPX socket. Used in conjunction with 
<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a> function calls that specify IPX_SPXGETCONNECTIONSTATUS in the <i>optname</i> parameter. All numbers in 
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




<a href="https://msdn.microsoft.com/25bc511d-7a9f-41c1-8983-1af1e3f8bf2d">getsockopt</a>
 

 

