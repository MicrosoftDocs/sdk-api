---
UID: NS:dhcpsapi._DHCP_IP_RANGE
title: "_DHCP_IP_RANGE"
author: windows-driver-content
description: The DHCP_IP_RANGE structure defines a range of IP addresses.
old-location: dhcp\dhcp_ip_range.htm
old-project: DHCP
ms.assetid: 8d3f021d-25ac-44de-9bbc-cc558bc47f91
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDHCP_IP_RANGE, DHCP_IP_RANGE, DHCP_IP_RANGE structure [DHCP], LPDHCP_IP_RANGE, LPDHCP_IP_RANGE structure pointer [DHCP], _DHCP_IP_RANGE, dhcp.dhcp_ip_range, dhcpsapi/LPDHCP_IP_RANGE, dhcpsapi/_DHCP_IP_RANGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCP_IP_RANGE, *LPDHCP_IP_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_IP_RANGE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_IP_RANGE structure


## -description


The <b>DHCP_IP_RANGE</b> structure defines a range of IP addresses.


## -struct-fields




### -field StartAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the first IP address in the range.


### -field EndAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the last IP address in the range.

