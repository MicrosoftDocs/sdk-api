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

# PxeDhcpv6ParseRelayForw function


## -description


This function can be used by a provider to parse RELAY-FORW messages and their nested OPTION_RELAY_MSG messages.   The information returned can be used to construct a RELAY-REPL packet using the <a href="https://msdn.microsoft.com/0FE31279-64CA-4B5E-87E4-6BD035A59A02">PxeDhcpv6CreateRelayRepl</a> function.  

For more information about RELAY-FORW and OPTION_RELAY_MSG messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -parameters




### -param pRelayForwPacket [in]

Specifies a pointer to a DHCPv6 RELAY-FORW message.


### -param uRelayForwPacketLen [in]

The size in bytes of the RELAY-FORW message pointed to by the <i>pRelayForwPacket</i> parameter.


### -param pRelayMessages [out]

An array of <a href="https://msdn.microsoft.com/BD796237-8ADE-45EC-9436-7BE2BC2C2D4E">PXE_DHCPV6_NESTED_RELAY_MESSAGE</a> structures initialized by this routine.  The array’s size is specified by <i>nRelayMessages</i>.  Elements of this array are initialized to point to the nested chain of relay packets encoded in OPTION_RELAY_MSG.  Index 0 is the outermost nested OPTION_RELAY_MSG packet. As the index increases the pointers correspond to more deeply nested OPTION_RELAY_MSG packets.




### -param nRelayMessages [in]

The size of the array, in number of array elements, pointed to by the <i>pRelayMessages</i> parameter.




### -param pnRelayMessages [out]

Specifies a pointer to a <b>ULONG</b> value which on success receives the actual number of elements written into the <i>pRelayMessages</i> array.




### -param ppInnerPacket [out]

Specifies a pointer to a <b>PVOID</b> value which on success is set to the start of the innermost packet in the relay chain. This is the original client request packet.


### -param pcbInnerPacket [out]

Specifies a pointer to a <b>ULONG</b> value which on success will be set to the size, in bytes, of the innermost packet in the relay chain which is the original client request packet.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



