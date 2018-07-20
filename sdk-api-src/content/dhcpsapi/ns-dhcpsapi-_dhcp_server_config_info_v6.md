---
UID: NS:dhcpsapi._DHCP_SERVER_CONFIG_INFO_V6
title: "_DHCP_SERVER_CONFIG_INFO_V6"
author: windows-sdk-content
description: Contains the settings for the DHCPv6 server.
old-location: dhcp\dhcp_server_config_info_v6.htm
old-project: dhcp
ms.assetid: 9862f0c1-3c42-4ad7-af3c-15868e4a9314
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPDHCP_SERVER_CONFIG_INFO_V6, DHCP_SERVER_CONFIG_INFO_V6, DHCP_SERVER_CONFIG_INFO_V6 structure [DHCP], PDHCP_SERVER_CONFIG_INFO_V6, PDHCP_SERVER_CONFIG_INFO_V6 structure pointer [DHCP], _DHCP_SERVER_CONFIG_INFO_V6, dhcp.dhcp_server_config_info_v6, dhcpsapi/DHCP_SERVER_CONFIG_INFO_V6, dhcpsapi/PDHCP_SERVER_CONFIG_INFO_V6"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DHCP_SERVER_CONFIG_INFO_V6, *LPDHCP_SERVER_CONFIG_INFO_V6
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SERVER_CONFIG_INFO_V6
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SERVER_CONFIG_INFO_V6 structure


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

