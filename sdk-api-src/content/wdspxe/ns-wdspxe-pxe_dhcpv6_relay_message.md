---
UID: NS:wdspxe.tagPXE_DHCPV6_RELAY_MESSAGE
title: PXE_DHCPV6_RELAY_MESSAGE (wdspxe.h)
author: windows-sdk-content
description: Provides the DHCPV6 relay message.
old-location: wds\pxe_dhcpv6_relay_message.htm
tech.root: wds
ms.assetid: 6C27D67D-938B-4357-9664-704FC04DCFBB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPXE_DHCPV6_RELAY_MESSAGE, PPXE_DHCPV6_RELAY_MESSAGE, PPXE_DHCPV6_RELAY_MESSAGE structure pointer [Windows Deployment Services], PXE_DHCPV6_RELAY_MESSAGE, PXE_DHCPV6_RELAY_MESSAGE structure [Windows Deployment Services], wds.pxe_dhcpv6_relay_message, wdspxe/PPXE_DHCPV6_RELAY_MESSAGE, wdspxe/PXE_DHCPV6_RELAY_MESSAGE"
ms.topic: struct
f1_keywords: 
 - "wdspxe/PXE_DHCPV6_RELAY_MESSAGE"
dev_langs:
 - c++
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
 - PXE_DHCPV6_RELAY_MESSAGE
targetos: Windows
req.typenames: PXE_DHCPV6_RELAY_MESSAGE, *PPXE_DHCPV6_RELAY_MESSAGE
req.redist: 
ms.custom: 19H1
---

# PXE_DHCPV6_RELAY_MESSAGE structure


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

A <a href="https://docs.microsoft.com/windows/desktop/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option">PXE_DHCPV6_OPTION</a> structure and see RFC 3315 section 7.

