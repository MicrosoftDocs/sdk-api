---
UID: NS:dhcpsapi._DHCP_IP_RANGE
title: DHCP_IP_RANGE (dhcpsapi.h)
description: The DHCP_IP_RANGE structure defines a range of IP addresses.
helpviewer_keywords: ["*LPDHCP_IP_RANGE","DHCP_IP_RANGE","DHCP_IP_RANGE structure [DHCP]","LPDHCP_IP_RANGE","LPDHCP_IP_RANGE structure pointer [DHCP]","dhcp.dhcp_ip_range","dhcpsapi/LPDHCP_IP_RANGE","dhcpsapi/_DHCP_IP_RANGE"]
old-location: dhcp\dhcp_ip_range.htm
tech.root: DHCP
ms.assetid: 8d3f021d-25ac-44de-9bbc-cc558bc47f91
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_IP_RANGE, DHCP_IP_RANGE, DHCP_IP_RANGE structure [DHCP], LPDHCP_IP_RANGE, LPDHCP_IP_RANGE structure pointer [DHCP], dhcp.dhcp_ip_range, dhcpsapi/LPDHCP_IP_RANGE, dhcpsapi/_DHCP_IP_RANGE'
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
req.typenames: DHCP_IP_RANGE, *LPDHCP_IP_RANGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_IP_RANGE
 - dhcpsapi/_DHCP_IP_RANGE
 - LPDHCP_IP_RANGE
 - dhcpsapi/LPDHCP_IP_RANGE
 - DHCP_IP_RANGE
 - dhcpsapi/DHCP_IP_RANGE
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
 - DHCP_IP_RANGE
---

# DHCP_IP_RANGE structure


## -description

The <b>DHCP_IP_RANGE</b> structure defines a range of IP addresses.

## -struct-fields

### -field StartAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the first IP address in the range.

### -field EndAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the last IP address in the range.