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

# tagPXE_DHCPV6_RELAY_MESSAGE structure


## -description


Provides the DHCPV6 relay message.

MessageType, HopCount, LinkAddress, and Options fields that are described by RFC 3315 section 7.

For more information about DHCPV6 message type, hop count, link address, and options, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -struct-fields




### -field MessageType

The message type


### -field HopCount

The hop count


### -field LinkAddress

The link address


### -field PeerAddress

The peer address


### -field Options

A <a href="https://msdn.microsoft.com/9B0A1A5B-1CF7-46B4-9C94-42355555DD60">PXE_DHCPV6_OPTION</a> structure and see RFC 3315 section 7.

