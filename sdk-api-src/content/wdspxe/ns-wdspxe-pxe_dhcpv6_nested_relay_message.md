---
UID: NS:wdspxe.tagPXE_DHCPV6_NESTED_RELAY_MESSAGE
title: PXE_DHCPV6_NESTED_RELAY_MESSAGE (wdspxe.h)
description: Describes packets nested in OPTION_RELAY_MSG message.
helpviewer_keywords: ["*PPXE_DHCPV6_NESTED_RELAY_MESSAGE","PPXE_DHCPV6_NESTED_RELAY_MESSAGE","PPXE_DHCPV6_NESTED_RELAY_MESSAGE structure pointer [Windows Deployment Services]","PXE_DHCPV6_NESTED_RELAY_MESSAGE","PXE_DHCPV6_NESTED_RELAY_MESSAGE structure [Windows Deployment Services]","wds.pxe_dhcpv6_nested_relay_message","wdspxe/PPXE_DHCPV6_NESTED_RELAY_MESSAGE","wdspxe/PXE_DHCPV6_NESTED_RELAY_MESSAGE"]
old-location: wds\pxe_dhcpv6_nested_relay_message.htm
tech.root: wds
ms.assetid: BD796237-8ADE-45EC-9436-7BE2BC2C2D4E
ms.date: 12/05/2018
ms.keywords: '*PPXE_DHCPV6_NESTED_RELAY_MESSAGE, PPXE_DHCPV6_NESTED_RELAY_MESSAGE, PPXE_DHCPV6_NESTED_RELAY_MESSAGE structure pointer [Windows Deployment Services], PXE_DHCPV6_NESTED_RELAY_MESSAGE, PXE_DHCPV6_NESTED_RELAY_MESSAGE structure [Windows Deployment Services], wds.pxe_dhcpv6_nested_relay_message, wdspxe/PPXE_DHCPV6_NESTED_RELAY_MESSAGE, wdspxe/PXE_DHCPV6_NESTED_RELAY_MESSAGE'
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
req.typenames: PXE_DHCPV6_NESTED_RELAY_MESSAGE, *PPXE_DHCPV6_NESTED_RELAY_MESSAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPXE_DHCPV6_NESTED_RELAY_MESSAGE
 - wdspxe/tagPXE_DHCPV6_NESTED_RELAY_MESSAGE
 - PPXE_DHCPV6_NESTED_RELAY_MESSAGE
 - wdspxe/PPXE_DHCPV6_NESTED_RELAY_MESSAGE
 - PXE_DHCPV6_NESTED_RELAY_MESSAGE
 - wdspxe/PXE_DHCPV6_NESTED_RELAY_MESSAGE
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
 - PXE_DHCPV6_NESTED_RELAY_MESSAGE
---

# PXE_DHCPV6_NESTED_RELAY_MESSAGE structure


## -description

Describes packets nested in OPTION_RELAY_MSG message.

For more information about OPTION_RELAY_MSG and RELAY-FORW messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="https://www.ietf.org/rfc/rfc3315.txt">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).

## -struct-fields

### -field pRelayMessage

A pointer to the nested RELAY-FORW message.

### -field cbRelayMessage

A pointer to the size of the nested RELAY-FORW message.

### -field pInterfaceIdOption

If the nested RELAY-FORW message contains <b>OPTION_INTERFACE_ID</b>, this  is a pointer to the option payload. Otherwise, this field will be <b>NULL</b>.

### -field cbInterfaceIdOption

If the nested RELAY-FORW message contains <b>OPTION_INTERFACE_ID</b>, this  is the size of the option payload.
     Otherwise, this field will be 0.

