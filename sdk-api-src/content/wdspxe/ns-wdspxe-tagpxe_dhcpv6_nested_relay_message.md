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

