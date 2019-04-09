---
UID: NS:wdspxe.tagPXE_DHCPV6_MESSAGE
title: PXE_DHCPV6_MESSAGE (wdspxe.h)
author: windows-sdk-content
description: A DHCPV6 message.
old-location: wds\pxe_dhcpv6_message.htm
tech.root: wds
ms.assetid: FA9CE377-8C66-4873-B6EF-5761FF398164
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PPXE_DHCPV6_MESSAGE, PPXE_DHCPV6_MESSAGE, PPXE_DHCPV6_MESSAGE structure pointer [Windows Deployment Services], PXE_DHCPV6_MESSAGE, PXE_DHCPV6_MESSAGE structure [Windows Deployment Services], wds.pxe_dhcpv6_message, wdspxe/PPXE_DHCPV6_MESSAGE, wdspxe/PXE_DHCPV6_MESSAGE"
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
 - PXE_DHCPV6_MESSAGE
product: Windows
targetos: Windows
req.typenames: PXE_DHCPV6_MESSAGE, *PPXE_DHCPV6_MESSAGE
req.redist: 
---

# PXE_DHCPV6_MESSAGE structure


## -description


A DHCPV6 message.

For more information about the DHCPv6 messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -struct-fields




### -field MessageType

The DHCPv6 message type.


### -field TransactionIDByte1

Byte 1  of the transaction-id in the DHCPv6 message.


### -field TransactionIDByte2

Byte 2  of the transaction-id  the DHCPv6 message.


### -field TransactionIDByte3

Byte 3  of the transaction-id DHCPv6 message.


### -field Options

A <a href="https://msdn.microsoft.com/9B0A1A5B-1CF7-46B4-9C94-42355555DD60">PXE_DHCPV6_OPTION</a> structure that specifies the DHCPV6 option.

