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

# tagPXE_DHCPV6_MESSAGE_HEADER structure


## -description


Describes the fields in common between the  <a href="https://msdn.microsoft.com/FA9CE377-8C66-4873-B6EF-5761FF398164">PXE_DHCPV6_MESSAGE</a> and <a href="https://msdn.microsoft.com/6C27D67D-938B-4357-9664-704FC04DCFBB">PXE_DHCPV6_RELAY_MESSAGE</a> structures.

For more information about the DHCPv6 messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -struct-fields




### -field MessageType

The DHCPv6 Message Type.


### -field Message

The remainder of the packet which must be interpreted differently based on the <b>MessageType</b>.



