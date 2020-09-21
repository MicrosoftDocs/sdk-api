---
UID: NS:dhcpsapi._DHCP_RESERVATION_INFO_ARRAY
title: DHCP_RESERVATION_INFO_ARRAY (dhcpsapi.h)
description: The DHCP_RESERVATION_INFO_ARRAY structure defines an array of IPv4 reservations for DHCPv4 clients.
helpviewer_keywords: ["*LPDHCP_RESERVATION_INFO_ARRAY","DHCP_RESERVATION_INFO_ARRAY","DHCP_RESERVATION_INFO_ARRAY structure [DHCP]","LPDHCP_RESERVATION_INFO_ARRAY","LPDHCP_RESERVATION_INFO_ARRAY structure pointer [DHCP]","dhcp.dhcp_reservation_info_array","dhcpsapi/DHCP_RESERVATION_INFO_ARRAY","dhcpsapi/LPDHCP_RESERVATION_INFO_ARRAY"]
old-location: dhcp\dhcp_reservation_info_array.htm
tech.root: DHCP
ms.assetid: 9823ee47-6b61-4256-8fac-d301d72774ec
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_RESERVATION_INFO_ARRAY, DHCP_RESERVATION_INFO_ARRAY, DHCP_RESERVATION_INFO_ARRAY structure [DHCP], LPDHCP_RESERVATION_INFO_ARRAY, LPDHCP_RESERVATION_INFO_ARRAY structure pointer [DHCP], dhcp.dhcp_reservation_info_array, dhcpsapi/DHCP_RESERVATION_INFO_ARRAY, dhcpsapi/LPDHCP_RESERVATION_INFO_ARRAY'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: DHCP_RESERVATION_INFO_ARRAY, *LPDHCP_RESERVATION_INFO_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_RESERVATION_INFO_ARRAY
 - dhcpsapi/_DHCP_RESERVATION_INFO_ARRAY
 - LPDHCP_RESERVATION_INFO_ARRAY
 - dhcpsapi/LPDHCP_RESERVATION_INFO_ARRAY
 - DHCP_RESERVATION_INFO_ARRAY
 - dhcpsapi/DHCP_RESERVATION_INFO_ARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_RESERVATION_INFO_ARRAY
---

# DHCP_RESERVATION_INFO_ARRAY structure


## -description

The <b>DHCP_RESERVATION_INFO_ARRAY</b> structure defines an array of IPv4 reservations for DHCPv4 clients.

## -struct-fields

### -field NumElements

Integer that specifies the number of IPv4 client reservations in <b>Elements</b>.

### -field Elements

Pointer to an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_reservation_info">DHCP_IP_RESERVATION_INFO</a> structures that contain IPv4 client reservations.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4enumsubnetreservations">DhcpV4EnumSubnetReservations</a>