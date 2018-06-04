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

# PxeDhcpv6Initialize function


## -description


Initializes a response packet as a DHCPv6 reply packet.

For RELAY-FORW messages, this function initializes the message type, hop count, link address and peer address.  For other DHCPv6 request types, this function initializes the message type and transaction ID.  In all cases, the option payload of the produced packet will be empty.

For more information about RELAY-FORW messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -parameters




### -param pRequest [in]

Address of a valid DHCPv6 packet received from the client in the 
      <a href="https://msdn.microsoft.com/704972d5-177a-490e-881f-d2b3025babda">PxeProviderRecvRequest</a> callback.


### -param cbRequest [in]

Length of the packet pointed to by the <i>pRequest</i> parameter.


### -param pReply [in, out]

Pointer to a reply packet allocated with 
      the <a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a> function.


### -param cbReply [in]

Allocated length of the packet pointed to by the <i>pReply</i> parameter.


### -param pcbReplyUsed [out]

Address of a <b>ULONG</b> that on successful completion will receive the length of 
      the packet pointed to by the <i>pReply</i> parameter.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



