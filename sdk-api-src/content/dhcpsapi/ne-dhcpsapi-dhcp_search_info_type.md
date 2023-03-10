---
UID: NE:dhcpsapi._DHCP_CLIENT_SEARCH_TYPE
title: DHCP_SEARCH_INFO_TYPE (dhcpsapi.h)
description: Defines the set of possible attributes used to search DHCP client information records.
helpviewer_keywords: ["*LPDHCP_SEARCH_INFO_TYPE","DHCP_SEARCH_INFO_TYPE","DHCP_SEARCH_INFO_TYPE enumeration [DHCP]","DhcpClientHardwareAddress","DhcpClientIpAddress","DhcpClientName","LPDHCP_SEARCH_INFO_TYPE","LPDHCP_SEARCH_INFO_TYPE enumeration pointer [DHCP]","dhcp.dhcp_search_info_type","dhcpsapi/DHCP_SEARCH_INFO_TYPE","dhcpsapi/DhcpClientHardwareAddress","dhcpsapi/DhcpClientIpAddress","dhcpsapi/DhcpClientName","dhcpsapi/LPDHCP_SEARCH_INFO_TYPE"]
old-location: dhcp\dhcp_search_info_type.htm
tech.root: DHCP
ms.assetid: b635ea03-689c-4471-bff2-72fceec78440
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SEARCH_INFO_TYPE, DHCP_SEARCH_INFO_TYPE, DHCP_SEARCH_INFO_TYPE enumeration [DHCP], DhcpClientHardwareAddress, DhcpClientIpAddress, DhcpClientName, LPDHCP_SEARCH_INFO_TYPE, LPDHCP_SEARCH_INFO_TYPE enumeration pointer [DHCP], dhcp.dhcp_search_info_type, dhcpsapi/DHCP_SEARCH_INFO_TYPE, dhcpsapi/DhcpClientHardwareAddress, dhcpsapi/DhcpClientIpAddress, dhcpsapi/DhcpClientName, dhcpsapi/LPDHCP_SEARCH_INFO_TYPE'
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
req.typenames: DHCP_SEARCH_INFO_TYPE, *LPDHCP_SEARCH_INFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_SEARCH_TYPE
 - dhcpsapi/_DHCP_CLIENT_SEARCH_TYPE
 - LPDHCP_SEARCH_INFO_TYPE
 - dhcpsapi/LPDHCP_SEARCH_INFO_TYPE
 - DHCP_SEARCH_INFO_TYPE
 - dhcpsapi/DHCP_SEARCH_INFO_TYPE
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
 - DHCP_SEARCH_INFO_TYPE
---

# DHCP_SEARCH_INFO_TYPE enumeration


## -description

The <b>DHCP_SEARCH_INFO_TYPE</b> enumeration defines the set of possible attributes used to search DHCP client information records.

## -enum-fields

### -field DhcpClientIpAddress

The search will be performed against the assigned DHCP client IP address, represented as a 32-bit unsigned integer value.

### -field DhcpClientHardwareAddress

The search will be performed against the MAC address of the DHCP client network interface device, represented as a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a> structure.

### -field DhcpClientName

The search will be performed against the DHCP client's network name, represented as a Unicode string.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_BINARY_DATA</a>



<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a>