---
UID: NS:dhcpsapi._DHCP_BOOTP_IP_RANGE
title: "_DHCP_BOOTP_IP_RANGE"
author: windows-sdk-content
description: The DHCP_BOOTP_IP_RANGE structure defines a suite of IPs for lease to BOOTP-specific clients.
old-location: dhcp\dhcp_bootp_ip_range.htm
tech.root: DHCP
ms.assetid: 23268029-0b49-4fd4-8410-4bac6c8ad151
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_BOOT_IP_RANGE, DHCP_BOOTP_IP_RANGE, DHCP_BOOTP_IP_RANGE structure [DHCP], LPDHCP_BOOT_IP_RANGE, LPDHCP_BOOT_IP_RANGE structure pointer [DHCP], _DHCP_BOOTP_IP_RANGE, dhcp.dhcp_bootp_ip_range, dhcpsapi/LPDHCP_BOOT_IP_RANGE, dhcpsapi/_DHCP_BOOTP_IP_RANGE"
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
 - DHCP_BOOTP_IP_RANGE
product: Windows
targetos: Windows
req.typenames: DHCP_BOOTP_IP_RANGE, *LPDHCP_BOOT_IP_RANGE
req.redist: 
---

# _DHCP_BOOTP_IP_RANGE structure


## -description


The <b>DHCP_BOOTP_IP_RANGE</b> structure defines a suite of IPs for lease to BOOTP-specific clients.


## -struct-fields




### -field StartAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the start of the IP range used for BOOTP service.


### -field EndAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the end of the IP range used for BOOTP service.


### -field BootpAllocated

Specifies the number of BOOTP clients with addresses served from this range.


### -field MaxBootpAllowed

Specifies the maximum number of BOOTP clients this range is allowed to serve.

