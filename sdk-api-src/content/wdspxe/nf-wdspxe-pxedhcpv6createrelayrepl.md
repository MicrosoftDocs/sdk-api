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

# PxeDhcpv6CreateRelayRepl function


## -description


Generates a RELAY-REPL message.

For more information about RELAY-REPL and RELAY-FORW messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -parameters




### -param pRelayMessages [in]

An array of <b>PXE_DHCPV6_NESTED_RELAY_FORW</b> structures which together specify the sequence of nested RELAY-FORW packets.  This value can be obtained from the <i>pRelayMessages</i> parameter of <a href="https://msdn.microsoft.com/1D9F1FFF-3ABB-4580-A5F2-C74B5E7EEAC9">PxeDhcpv6ParseRelayForw</a>.


### -param nRelayMessages [in]

The number of elements in the array pointed to by the <i>pRelayMessages</i> argument.


### -param pInnerPacket [in]

A pointer to a packet which is the server’s response to the innermost packet in the RELAY-FORW chain.


### -param cbInnerPacket [in]

The size of the packet pointed to by the <i>pInnerPacket</i> argument.


### -param pReplyBuffer [out]

A pointer to a buffer used to construct the outer RELAY-REPL packet. This buffer receives the nested response packet and the nested RELAY-REPL chain specified by the <i>pRelayMessages</i> parameter.


### -param cbReplyBuffer [in]

The size of the buffer in bytes  pointed to by <i>pRelyBuffer</i>.


### -param pcbReplyBuffer [out]

On success, this is set to the actual size of the RELAY-REPL packet in the buffer pointed to by <i>pRelyBuffer</i>.  


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



