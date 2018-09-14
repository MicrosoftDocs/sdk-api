---
UID: NS:wdspxe.tagPXE_DHCPV6_MESSAGE_HEADER
title: tagPXE_DHCPV6_MESSAGE_HEADER
author: windows-sdk-content
description: Describes the fields in common between the PXE_DHCPV6_MESSAGE and PXE_DHCPV6_RELAY_MESSAGE structures.
old-location: wds\pxe_dhcpv6_message_header.htm
tech.root: wds
ms.assetid: D6D387EB-85CC-413E-926D-A222274ABD52
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: "*PPXE_DHCPV6_MESSAGE_HEADER, PPXE_DHCPV6_MESSAGE_HEADER, PPXE_DHCPV6_MESSAGE_HEADER structure pointer [Windows Deployment Services], PXE_DHCPV6_MESSAGE_HEADER, PXE_DHCPV6_MESSAGE_HEADER structure [Windows Deployment Services], tagPXE_DHCPV6_MESSAGE_HEADER, wds.pxe_dhcpv6_message_header, wdspxe/PPXE_DHCPV6_MESSAGE_HEADER, wdspxe/PXE_DHCPV6_MESSAGE_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_DHCPV6_MESSAGE_HEADER
product: Windows
targetos: Windows
req.typenames: PXE_DHCPV6_MESSAGE_HEADER, *PPXE_DHCPV6_MESSAGE_HEADER
req.redist: 
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



