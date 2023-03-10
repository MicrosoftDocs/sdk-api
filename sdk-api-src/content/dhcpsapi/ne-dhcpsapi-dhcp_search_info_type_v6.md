---
UID: NE:dhcpsapi._DHCP_CLIENT_SEARCH_TYPE_V6
title: DHCP_SEARCH_INFO_TYPE_V6 (dhcpsapi.h)
description: Defines the set of possible attributes used to search DHCPv6 client information records.
helpviewer_keywords: ["*LPDHCP_SEARCH_INFO_TYPE_V6","DHCP_SEARCH_INFO_TYPE_V6","DHCP_SEARCH_INFO_TYPE_V6 enumeration [DHCP]","Dhcpv6ClientDUID","Dhcpv6ClientIpAddress","Dhcpv6ClientName","LPDHCP_SEARCH_INFO_TYPE_V6","LPDHCP_SEARCH_INFO_TYPE_V6 enumeration pointer [DHCP]","dhcp.dhcp_search_info_type_v6","dhcpsapi/DHCP_SEARCH_INFO_TYPE_V6","dhcpsapi/Dhcpv6ClientDUID","dhcpsapi/Dhcpv6ClientIpAddress","dhcpsapi/Dhcpv6ClientName","dhcpsapi/LPDHCP_SEARCH_INFO_TYPE_V6"]
old-location: dhcp\dhcp_search_info_type_v6.htm
tech.root: DHCP
ms.assetid: 56c2cbda-4af5-4f28-9b1f-be7d6cf0c1f5
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SEARCH_INFO_TYPE_V6, DHCP_SEARCH_INFO_TYPE_V6, DHCP_SEARCH_INFO_TYPE_V6 enumeration [DHCP], Dhcpv6ClientDUID, Dhcpv6ClientIpAddress, Dhcpv6ClientName, LPDHCP_SEARCH_INFO_TYPE_V6, LPDHCP_SEARCH_INFO_TYPE_V6 enumeration pointer [DHCP], dhcp.dhcp_search_info_type_v6, dhcpsapi/DHCP_SEARCH_INFO_TYPE_V6, dhcpsapi/Dhcpv6ClientDUID, dhcpsapi/Dhcpv6ClientIpAddress, dhcpsapi/Dhcpv6ClientName, dhcpsapi/LPDHCP_SEARCH_INFO_TYPE_V6'
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
targetos: Windows
req.typenames: DHCP_SEARCH_INFO_TYPE_V6, *LPDHCP_SEARCH_INFO_TYPE_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_SEARCH_TYPE_V6
 - dhcpsapi/_DHCP_CLIENT_SEARCH_TYPE_V6
 - LPDHCP_SEARCH_INFO_TYPE_V6
 - dhcpsapi/LPDHCP_SEARCH_INFO_TYPE_V6
 - DHCP_SEARCH_INFO_TYPE_V6
 - dhcpsapi/DHCP_SEARCH_INFO_TYPE_V6
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
 - DHCP_SEARCH_INFO_TYPE_V6
---

# DHCP_SEARCH_INFO_TYPE_V6 enumeration


## -description

The <b>DHCP_SEARCH_INFO_TYPE_V6</b> enumeration defines the set of possible attributes used to search DHCPv6 client information records.

## -enum-fields

### -field Dhcpv6ClientIpAddress

The search will be performed against the assigned DHCPv6 client IPv6 address.

### -field Dhcpv6ClientDUID

The search will be performed against the DHCPv6 client's DHCP unique ID, represented as a GUID.

### -field Dhcpv6ClientName

The search will be performed against the DHCP client's network name, represented as a Unicode string.

