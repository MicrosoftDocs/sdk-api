---
UID: NS:wdspxe.tagPXE_DHCPV6_MESSAGE_HEADER
title: PXE_DHCPV6_MESSAGE_HEADER (wdspxe.h)
description: Describes the fields in common between the PXE_DHCPV6_MESSAGE and PXE_DHCPV6_RELAY_MESSAGE structures.
helpviewer_keywords: ["*PPXE_DHCPV6_MESSAGE_HEADER","PPXE_DHCPV6_MESSAGE_HEADER","PPXE_DHCPV6_MESSAGE_HEADER structure pointer [Windows Deployment Services]","PXE_DHCPV6_MESSAGE_HEADER","PXE_DHCPV6_MESSAGE_HEADER structure [Windows Deployment Services]","wds.pxe_dhcpv6_message_header","wdspxe/PPXE_DHCPV6_MESSAGE_HEADER","wdspxe/PXE_DHCPV6_MESSAGE_HEADER"]
old-location: wds\pxe_dhcpv6_message_header.htm
tech.root: wds
ms.assetid: D6D387EB-85CC-413E-926D-A222274ABD52
ms.date: 12/05/2018
ms.keywords: '*PPXE_DHCPV6_MESSAGE_HEADER, PPXE_DHCPV6_MESSAGE_HEADER, PPXE_DHCPV6_MESSAGE_HEADER structure pointer [Windows Deployment Services], PXE_DHCPV6_MESSAGE_HEADER, PXE_DHCPV6_MESSAGE_HEADER structure [Windows Deployment Services], wds.pxe_dhcpv6_message_header, wdspxe/PPXE_DHCPV6_MESSAGE_HEADER, wdspxe/PXE_DHCPV6_MESSAGE_HEADER'
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
targetos: Windows
req.typenames: PXE_DHCPV6_MESSAGE_HEADER, *PPXE_DHCPV6_MESSAGE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPXE_DHCPV6_MESSAGE_HEADER
 - wdspxe/tagPXE_DHCPV6_MESSAGE_HEADER
 - PPXE_DHCPV6_MESSAGE_HEADER
 - wdspxe/PPXE_DHCPV6_MESSAGE_HEADER
 - PXE_DHCPV6_MESSAGE_HEADER
 - wdspxe/PXE_DHCPV6_MESSAGE_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_DHCPV6_MESSAGE_HEADER
---

# PXE_DHCPV6_MESSAGE_HEADER structure


## -description

Describes the fields in common between the  <a href="/windows/desktop/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message">PXE_DHCPV6_MESSAGE</a> and <a href="/windows/desktop/api/wdspxe/ns-wdspxe-pxe_dhcpv6_relay_message">PXE_DHCPV6_RELAY_MESSAGE</a> structures.

For more information about the DHCPv6 messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="https://www.ietf.org/rfc/rfc3315.txt">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).

## -struct-fields

### -field MessageType

The DHCPv6 Message Type.

### -field Message

The remainder of the packet which must be interpreted differently based on the <b>MessageType</b>.