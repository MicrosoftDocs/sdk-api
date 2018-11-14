---
UID: NS:dhcpsapi._DHCP_ADDR_PATTERN
title: "_DHCP_ADDR_PATTERN"
author: windows-sdk-content
description: Contains the information regarding the link-layer address/pattern.
old-location: dhcp\dhcp_addr_pattern.htm
tech.root: DHCP
ms.assetid: 8c645b03-9859-48e9-8974-2dbdc9cfcac6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDHCP_ADDR_PATTERN, DHCP_ADDR_PATTERN, DHCP_ADDR_PATTERN structure [DHCP], PDHCP_ADDR_PATTERN, PDHCP_ADDR_PATTERN structure pointer [DHCP], _DHCP_ADDR_PATTERN, dhcp.dhcp_addr_pattern, dhcpsapi/DHCP_ADDR_PATTERN, dhcpsapi/PDHCP_ADDR_PATTERN"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Dhcpsapi.h
api_name:
 - DHCP_ADDR_PATTERN
product: Windows
targetos: Windows
req.typenames: DHCP_ADDR_PATTERN, *LPDHCP_ADDR_PATTERN
req.redist: 
---

# _DHCP_ADDR_PATTERN structure


## -description


The <b>DHCP_ADDR_PATTERN</b> structure contains the information regarding the link-layer address/pattern.


## -struct-fields




### -field MatchHWType

If <b>TRUE</b>, the hardware type member (<b>HWType</b>) will be matched; if <b>FALSE</b>, the hardware type member is ignored.


### -field HWType

8-bit integer value that specifies the hardware type of the address, specified in the pattern. Currently, only hardware type 1 (Ethernet 10 megabit) is supported as the filtering criterion.


### -field IsWildcard

 


### -field Length

8-bit integer value that contains the length of the pattern, in bytes.


### -field Pattern

Array of BYTE values that contain the pattern or hardware address.


#### - IsWildCard

If <b>TRUE</b>, <b>Pattern</b> contains a wildcard pattern; if <b>FALSE</b>, <b>Pattern</b> contains a hardware address.

