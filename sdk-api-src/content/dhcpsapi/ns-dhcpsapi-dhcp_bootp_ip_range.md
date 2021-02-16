---
UID: NS:dhcpsapi._DHCP_BOOTP_IP_RANGE
title: DHCP_BOOTP_IP_RANGE (dhcpsapi.h)
description: The DHCP_BOOTP_IP_RANGE structure defines a suite of IPs for lease to BOOTP-specific clients.
helpviewer_keywords: ["*LPDHCP_BOOT_IP_RANGE","DHCP_BOOTP_IP_RANGE","DHCP_BOOTP_IP_RANGE structure [DHCP]","LPDHCP_BOOT_IP_RANGE","LPDHCP_BOOT_IP_RANGE structure pointer [DHCP]","dhcp.dhcp_bootp_ip_range","dhcpsapi/LPDHCP_BOOT_IP_RANGE","dhcpsapi/_DHCP_BOOTP_IP_RANGE"]
old-location: dhcp\dhcp_bootp_ip_range.htm
tech.root: DHCP
ms.assetid: 23268029-0b49-4fd4-8410-4bac6c8ad151
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_BOOT_IP_RANGE, DHCP_BOOTP_IP_RANGE, DHCP_BOOTP_IP_RANGE structure [DHCP], LPDHCP_BOOT_IP_RANGE, LPDHCP_BOOT_IP_RANGE structure pointer [DHCP], dhcp.dhcp_bootp_ip_range, dhcpsapi/LPDHCP_BOOT_IP_RANGE, dhcpsapi/_DHCP_BOOTP_IP_RANGE'
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
targetos: Windows
req.typenames: DHCP_BOOTP_IP_RANGE, *LPDHCP_BOOT_IP_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_BOOTP_IP_RANGE
 - dhcpsapi/_DHCP_BOOTP_IP_RANGE
 - LPDHCP_BOOT_IP_RANGE
 - dhcpsapi/LPDHCP_BOOT_IP_RANGE
 - DHCP_BOOTP_IP_RANGE
 - dhcpsapi/DHCP_BOOTP_IP_RANGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_BOOTP_IP_RANGE
---

# DHCP_BOOTP_IP_RANGE structure


## -description

The <b>DHCP_BOOTP_IP_RANGE</b> structure defines a suite of IPs for lease to BOOTP-specific clients.

## -struct-fields

### -field StartAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the start of the IP range used for BOOTP service.

### -field EndAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the end of the IP range used for BOOTP service.

### -field BootpAllocated

Specifies the number of BOOTP clients with addresses served from this range.

### -field MaxBootpAllowed

Specifies the maximum number of BOOTP clients this range is allowed to serve.