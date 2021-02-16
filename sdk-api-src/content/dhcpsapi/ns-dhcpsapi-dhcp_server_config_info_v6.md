---
UID: NS:dhcpsapi._DHCP_SERVER_CONFIG_INFO_V6
title: DHCP_SERVER_CONFIG_INFO_V6 (dhcpsapi.h)
description: Contains the settings for the DHCPv6 server.
helpviewer_keywords: ["*LPDHCP_SERVER_CONFIG_INFO_V6","DHCP_SERVER_CONFIG_INFO_V6","DHCP_SERVER_CONFIG_INFO_V6 structure [DHCP]","PDHCP_SERVER_CONFIG_INFO_V6","PDHCP_SERVER_CONFIG_INFO_V6 structure pointer [DHCP]","dhcp.dhcp_server_config_info_v6","dhcpsapi/DHCP_SERVER_CONFIG_INFO_V6","dhcpsapi/PDHCP_SERVER_CONFIG_INFO_V6"]
old-location: dhcp\dhcp_server_config_info_v6.htm
tech.root: DHCP
ms.assetid: 9862f0c1-3c42-4ad7-af3c-15868e4a9314
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SERVER_CONFIG_INFO_V6, DHCP_SERVER_CONFIG_INFO_V6, DHCP_SERVER_CONFIG_INFO_V6 structure [DHCP], PDHCP_SERVER_CONFIG_INFO_V6, PDHCP_SERVER_CONFIG_INFO_V6 structure pointer [DHCP], dhcp.dhcp_server_config_info_v6, dhcpsapi/DHCP_SERVER_CONFIG_INFO_V6, dhcpsapi/PDHCP_SERVER_CONFIG_INFO_V6'
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
req.typenames: DHCP_SERVER_CONFIG_INFO_V6, *LPDHCP_SERVER_CONFIG_INFO_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SERVER_CONFIG_INFO_V6
 - dhcpsapi/_DHCP_SERVER_CONFIG_INFO_V6
 - LPDHCP_SERVER_CONFIG_INFO_V6
 - dhcpsapi/LPDHCP_SERVER_CONFIG_INFO_V6
 - DHCP_SERVER_CONFIG_INFO_V6
 - dhcpsapi/DHCP_SERVER_CONFIG_INFO_V6
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
 - DHCP_SERVER_CONFIG_INFO_V6
---

# DHCP_SERVER_CONFIG_INFO_V6 structure


## -description

The <b>DHCP_SERVER_CONFIG_INFO_V6</b> structure contains the settings for the DHCPv6 server.

## -struct-fields

### -field UnicastFlag

Reserved. This must to be set to 0.

### -field RapidCommitFlag

Reserved. This must to be set to 0.

### -field PreferredLifetime

Integer value that specifies the preferred lifetime for IANA addresses.

### -field ValidLifetime

Integer value that specifies the valid lifetime for IANA addresses.

### -field T1

Integer that specifies the value for time T1.

### -field T2

Integer that specifies the value for time T2.

### -field PreferredLifetimeIATA

The preferred lifetime value for a temporary IPv6 address. This is not used, and must to be set to 0.

### -field ValidLifetimeIATA

The valid lifetime value for a temporary IPv6 address. This is not used, and must to be set to 0.

### -field fAuditLog

If <b>TRUE</b>, audit logs are enabled on the DHCPv6 server; if <b>FALSE</b>, they are not.

