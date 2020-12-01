---
UID: NS:dhcpsapi._DHCP_MIB_INFO_V6
title: DHCP_MIB_INFO_V6 (dhcpsapi.h)
description: Contains statistics for the DHCPv6 server.
helpviewer_keywords: ["*LPDHCP_MIB_INFO_V6","DHCP_MIB_INFO_V6","DHCP_MIB_INFO_V6 structure [DHCP]","PDHCP_MIB_INFO_V6","PDHCP_MIB_INFO_V6 structure pointer [DHCP]","dhcp.dhcp_mib_info_v6","dhcpsapi/DHCP_MIB_INFO_V6","dhcpsapi/PDHCP_MIB_INFO_V6"]
old-location: dhcp\dhcp_mib_info_v6.htm
tech.root: DHCP
ms.assetid: 8b961666-4b55-47b4-be52-81b67c9d1cae
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_MIB_INFO_V6, DHCP_MIB_INFO_V6, DHCP_MIB_INFO_V6 structure [DHCP], PDHCP_MIB_INFO_V6, PDHCP_MIB_INFO_V6 structure pointer [DHCP], dhcp.dhcp_mib_info_v6, dhcpsapi/DHCP_MIB_INFO_V6, dhcpsapi/PDHCP_MIB_INFO_V6'
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
req.typenames: DHCP_MIB_INFO_V6, *LPDHCP_MIB_INFO_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_MIB_INFO_V6
 - dhcpsapi/_DHCP_MIB_INFO_V6
 - LPDHCP_MIB_INFO_V6
 - dhcpsapi/LPDHCP_MIB_INFO_V6
 - DHCP_MIB_INFO_V6
 - dhcpsapi/DHCP_MIB_INFO_V6
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
 - DHCP_MIB_INFO_V6
---

# DHCP_MIB_INFO_V6 structure


## -description

The <b>DHCP_MIB_INFO_V6</b> structure contains statistics for the DHCPv6 server.

## -struct-fields

### -field Solicits

Integer value that specifies the number of DHCPSOLICIT messages received by the DHCPv6 server from DHCPv6 clients.

### -field Advertises

Integer value that specifies the number of DHCPADVERTISE messages sent by DHCPv6 server to DHCPv6 clients.

### -field Requests

Integer value that specifies the number of DHCPREQUEST messages sent by DHCPv6 server to DHCPv6 clients.

### -field Renews

Integer value that specifies the number of DHCPRENEW messages sent by DHCPv6 server to DHCPv6 clients.

### -field Rebinds

Integer value that specifies the number of DHCPREBIND messages sent by DHCPv6 server to DHCPv6 clients.

### -field Replies

Integer value that specifies the number of DHCPREPLY messages sent by DHCPv6 server to DHCPv6 clients.

### -field Confirms

Integer value that specifies the number of DHCPCONFIRM messages sent by DHCPv6 server to DHCPv6 clients.

### -field Declines

Integer value that specifies the number of DHCPDECLINE messages sent by DHCPv6 server to DHCPv6 clients.

### -field Releases

Integer value that specifies the number of DHCPRELEASE messages sent by DHCPv6 server to DHCPv6 clients.

### -field Informs

Integer value that specifies the number of DHCPINFORM messages sent by DHCPv6 server to DHCPv6 clients.

### -field ServerStartTime

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-date_time">DATE_TIME</a> value that specifies the time the DHCPv6 server was started.

### -field Scopes

Integer value that contains the number of IPv6 scopes configured on the current DHCPv6 server. This member defines the number of DHCPv6 scopes in the subsequent member <b>ScopeInfo</b>.

### -field ScopeInfo

Pointer to an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-scope_mib_info">SCOPE_MIB_INFO</a> structures that contain statistics on individual scopes defined on the DHCPv6 server.

### -field ScopeInfo.size_is

### -field ScopeInfo.size_is.Scopes

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-scope_mib_info">SCOPE_MIB_INFO</a>