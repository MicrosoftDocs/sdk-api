---
UID: NS:dhcpsapi._DHCP_CLIENT_SEARCH_INFO_V6
title: DHCP_SEARCH_INFO_V6 (dhcpsapi.h)
description: Contains the term or value on which the DHCPv6 server database will be searched.
helpviewer_keywords: ["*LPDHCP_SEARCH_INFO_V6","DHCP_SEARCH_INFO_V6","DHCP_SEARCH_INFO_V6 structure [DHCP]","Dhcpv6ClientDUID","Dhcpv6ClientIpAddress","Dhcpv6ClientName","PDHCP_SEARCH_INFO_V6","PDHCP_SEARCH_INFO_V6 structure pointer [DHCP]","dhcp.dhcp_search_info_v6","dhcpsapi/DHCP_SEARCH_INFO_V6","dhcpsapi/PDHCP_SEARCH_INFO_V6"]
old-location: dhcp\dhcp_search_info_v6.htm
tech.root: DHCP
ms.assetid: b290baab-9a70-437a-a519-876891184fbc
ms.date: 11/19/2020
ms.keywords: '*LPDHCP_SEARCH_INFO_V6, DHCP_SEARCH_INFO_V6, DHCP_SEARCH_INFO_V6 structure [DHCP], Dhcpv6ClientDUID, Dhcpv6ClientIpAddress, Dhcpv6ClientName, PDHCP_SEARCH_INFO_V6, PDHCP_SEARCH_INFO_V6 structure pointer [DHCP], dhcp.dhcp_search_info_v6, dhcpsapi/DHCP_SEARCH_INFO_V6, dhcpsapi/PDHCP_SEARCH_INFO_V6'
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
req.typenames: DHCP_SEARCH_INFO_V6, *LPDHCP_SEARCH_INFO_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_SEARCH_INFO_V6
 - dhcpsapi/_DHCP_CLIENT_SEARCH_INFO_V6
 - LPDHCP_SEARCH_INFO_V6
 - dhcpsapi/LPDHCP_SEARCH_INFO_V6
 - DHCP_SEARCH_INFO_V6
 - dhcpsapi/DHCP_SEARCH_INFO_V6
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
 - DHCP_SEARCH_INFO_V6
---

# DHCP_SEARCH_INFO_V6 structure


## -description

The <b>DHCP_SEARCH_INFO_V6</b> structure contains the term or value on which the DHCPv6 server database will be searched.

## -struct-fields

### -field SearchType

Enumeration value that selects the type of the value on which the DHCPv6 database will be searched.


### SearchType - DHCP_SEARCH_INFO_V6 

Enumeration value that selects the type of the value on which the DHCPv6 database will be searched. 

* Dhcpv6ClientIpAddress

The search term value is a client's IPv6 address.

* Dhcpv6ClientDUID
 
The search term value is a client's DHCP unique ID (GUID). 

* Dhcpv6ClientName

The search term value is a client name string. 

### SearchInfo - union

* ClientIpAddress 

DHCP_IPV6_ADDRESS structure that specifies the client IPv6 address to search for.

* ClientDUI

DDHCP_CLIENT_UIDGUID value that specifies the client DHCP UID to search for.

* ClientName 

LPWSTRUnicode string that specifies the client name to search for. 



### -field SearchInfo.ClientIpAddress.case

### -field SearchInfo.ClientIpAddress.case.Dhcpv6ClientIpAddress

### -field SearchInfo.ClientDUID.case

### -field SearchInfo.ClientDUID.case.Dhcpv6ClientDUID

### -field SearchInfo.ClientName.case

### -field SearchInfo.ClientName.case.Dhcpv6ClientName



### -field SearchInfo.switch_type

### -field SearchInfo.switch_type.DHCP_SEARCH_INFO_TYPE_V6

### -field SearchInfo

### -field SearchInfo.ClientIpAddress

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that specifies the client IPv6 address to search for.

### -field SearchInfo.ClientDUID

GUID value that specifies the client DHCP UID to search for.

### -field SearchInfo.ClientName

Unicode string that specifies the client name to search for.

### -field _DHCP_CLIENT_SEARCH_UNION_V6

## -see-also

<a href="/windows/win32/api/dhcpsapi/ne-dhcpsapi-dhcp_search_info_type_v6">DHCP_SEARCH_INFO_TYPE_V6</a>