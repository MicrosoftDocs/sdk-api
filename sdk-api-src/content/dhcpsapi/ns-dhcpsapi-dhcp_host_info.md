---
UID: NS:dhcpsapi._DHCP_HOST_INFO
title: DHCP_HOST_INFO (dhcpsapi.h)
description: The DHCP_HOST_INFO structure defines information on a DHCP server (host).
helpviewer_keywords: ["*LPDHCP_HOST_INFO","DHCP_HOST_INFO","DHCP_HOST_INFO structure [DHCP]","LPDHCP_HOST_INFO","LPDHCP_HOST_INFO structure pointer [DHCP]","dhcp.dhcp_host_info","dhcpsapi/LPDHCP_HOST_INFO","dhcpsapi/_DHCP_HOST_INFO"]
old-location: dhcp\dhcp_host_info.htm
tech.root: DHCP
ms.assetid: 3d38f69d-2808-4e52-a3da-b6142578c981
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_HOST_INFO, DHCP_HOST_INFO, DHCP_HOST_INFO structure [DHCP], LPDHCP_HOST_INFO, LPDHCP_HOST_INFO structure pointer [DHCP], dhcp.dhcp_host_info, dhcpsapi/LPDHCP_HOST_INFO, dhcpsapi/_DHCP_HOST_INFO'
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
req.typenames: DHCP_HOST_INFO, *LPDHCP_HOST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_HOST_INFO
 - dhcpsapi/_DHCP_HOST_INFO
 - LPDHCP_HOST_INFO
 - dhcpsapi/LPDHCP_HOST_INFO
 - DHCP_HOST_INFO
 - dhcpsapi/DHCP_HOST_INFO
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
 - DHCP_HOST_INFO
---

# DHCP_HOST_INFO structure


## -description

The <b>DHCP_HOST_INFO</b> structure defines information on a DHCP server (host).

## -struct-fields

### -field IpAddress

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that contains the IP address of the DHCP server.

### -field NetBiosName

Unicode string that contains the NetBIOS name of the DHCP server.

### -field HostName

Unicode string that contains the network name of the DHCP server.

## -remarks

When this structure is populated by the DHCP Server, the <b>HostName</b> and <b>NetBiosName</b> members may be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v5">DHCP_SUBNET_ELEMENT_DATA_V5</a>