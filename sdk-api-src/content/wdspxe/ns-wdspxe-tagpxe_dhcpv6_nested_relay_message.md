---
UID: NS:wdspxe.tagPXE_DHCPV6_NESTED_RELAY_MESSAGE
title: tagPXE_DHCPV6_NESTED_RELAY_MESSAGE
author: windows-driver-content
description: Describes packets nested in OPTION_RELAY_MSG message.
old-location: wds\pxe_dhcpv6_nested_relay_message.htm
old-project: Wds
ms.assetid: BD796237-8ADE-45EC-9436-7BE2BC2C2D4E
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: "*PPXE_DHCPV6_NESTED_RELAY_MESSAGE, PPXE_DHCPV6_NESTED_RELAY_MESSAGE, PPXE_DHCPV6_NESTED_RELAY_MESSAGE structure pointer [Windows Deployment Services], PXE_DHCPV6_NESTED_RELAY_MESSAGE, PXE_DHCPV6_NESTED_RELAY_MESSAGE structure [Windows Deployment Services], tagPXE_DHCPV6_NESTED_RELAY_MESSAGE, wds.pxe_dhcpv6_nested_relay_message, wdspxe/PPXE_DHCPV6_NESTED_RELAY_MESSAGE, wdspxe/PXE_DHCPV6_NESTED_RELAY_MESSAGE"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PXE_DHCPV6_NESTED_RELAY_MESSAGE, *PPXE_DHCPV6_NESTED_RELAY_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WdsPxe.h
api_name:
-	PXE_DHCPV6_NESTED_RELAY_MESSAGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagPXE_DHCPV6_NESTED_RELAY_MESSAGE structure


## -description


Describes packets nested in OPTION_RELAY_MSG message.

For more information about OPTION_RELAY_MSG and RELAY-FORW messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


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

