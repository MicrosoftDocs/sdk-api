---
UID: NS:dhcpsapi._DHCP_IP_RESERVATION_V6
title: DHCP_IP_RESERVATION_V6 (dhcpsapi.h)
description: Defines an IPv6 reservation for a DHCPv6 client in a specific IPv6 prefix.
helpviewer_keywords: ["*LPDHCP_IP_RESERVATION_V6","DHCP_IP_RESERVATION_V6","DHCP_IP_RESERVATION_V6 structure [DHCP]","PDHCP_IP_RESERVATION_V6","PDHCP_IP_RESERVATION_V6 structure pointer [DHCP]","dhcp.dhcp_ip_reservation_v6","dhcpsapi/DHCP_IP_RESERVATION_V6","dhcpsapi/PDHCP_IP_RESERVATION_V6"]
old-location: dhcp\dhcp_ip_reservation_v6.htm
tech.root: DHCP
ms.assetid: f1595632-018b-4626-b3c6-49f0e5b3752c
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_IP_RESERVATION_V6, DHCP_IP_RESERVATION_V6, DHCP_IP_RESERVATION_V6 structure [DHCP], PDHCP_IP_RESERVATION_V6, PDHCP_IP_RESERVATION_V6 structure pointer [DHCP], dhcp.dhcp_ip_reservation_v6, dhcpsapi/DHCP_IP_RESERVATION_V6, dhcpsapi/PDHCP_IP_RESERVATION_V6'
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
req.typenames: DHCP_IP_RESERVATION_V6, *LPDHCP_IP_RESERVATION_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_IP_RESERVATION_V6
 - dhcpsapi/_DHCP_IP_RESERVATION_V6
 - LPDHCP_IP_RESERVATION_V6
 - dhcpsapi/LPDHCP_IP_RESERVATION_V6
 - DHCP_IP_RESERVATION_V6
 - dhcpsapi/DHCP_IP_RESERVATION_V6
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
 - DHCP_IP_RESERVATION_V6
---

# DHCP_IP_RESERVATION_V6 structure


## -description

The <b>DHCP_IP_RESERVATION_V6</b> structure defines an IPv6 reservation for a DHCPv6 client in a specific IPv6 prefix.

## -struct-fields

### -field ReservedIpAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 address of the DHCPv6 client for which an IPv6 reservation is created.

### -field ReservedForClient

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_binary_data">DHCP_CLIENT_UID</a> structure that contains the hardware address (MAC address) of the DHCPv6 client for which the IPv6 reservation is created.

### -field InterfaceId

Integer that specifies the interface identifier for which the IPv6 reservation is created.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_info">DHCP_IP_RESERVATION_INFO</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_v4">DHCP_IP_RESERVATION_V4</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v6">DHCP_SUBNET_ELEMENT_DATA_V6</a>