---
UID: NS:dhcpsapi._DHCP_HOST_INFO_V6
title: DHCP_HOST_INFO_V6 (dhcpsapi.h)
description: Contains network information about a DHCPv6 server (host), such as its IPv6 address and name.
helpviewer_keywords: ["*LPDHCP_HOST_INFO_V6","DHCP_HOST_INFO_V6","DHCP_HOST_INFO_V6 structure [DHCP]","PDHCP_HOST_INFO_V6","PDHCP_HOST_INFO_V6 structure pointer [DHCP]","dhcp.dhcp_host_info_v6","dhcpsapi/DHCP_HOST_INFO_V6","dhcpsapi/PDHCP_HOST_INFO_V6"]
old-location: dhcp\dhcp_host_info_v6.htm
tech.root: DHCP
ms.assetid: 7473bbcd-d032-4f44-96e8-e08f050c08a3
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_HOST_INFO_V6, DHCP_HOST_INFO_V6, DHCP_HOST_INFO_V6 structure [DHCP], PDHCP_HOST_INFO_V6, PDHCP_HOST_INFO_V6 structure pointer [DHCP], dhcp.dhcp_host_info_v6, dhcpsapi/DHCP_HOST_INFO_V6, dhcpsapi/PDHCP_HOST_INFO_V6'
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
req.typenames: DHCP_HOST_INFO_V6, *LPDHCP_HOST_INFO_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_HOST_INFO_V6
 - dhcpsapi/_DHCP_HOST_INFO_V6
 - LPDHCP_HOST_INFO_V6
 - dhcpsapi/LPDHCP_HOST_INFO_V6
 - DHCP_HOST_INFO_V6
 - dhcpsapi/DHCP_HOST_INFO_V6
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
 - DHCP_HOST_INFO_V6
---

# DHCP_HOST_INFO_V6 structure


## -description

The <b>DHCP_HOST_INFO_V6</b> structure contains network information about a DHCPv6 server (host), such as its IPv6 address and name.

## -struct-fields

### -field IpAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 address of the DHCPv6 server.

### -field NetBiosName

Pointer to a Unicode string that contains the NetBIOS name of the DHCPv6 server.

### -field HostName

Pointer to a Unicode string that contains the network name of the DHCPv6 server.

## -remarks

When this structure is populated by the DHCP Server, the <b>HostName</b> and <b>NetBiosName</b> members may be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a>