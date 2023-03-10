---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_ARRAY
title: DHCP_CLIENT_INFO_ARRAY (dhcpsapi.h)
description: The DHCP_CLIENT_INFO_ARRAY structure defines an array of DHCP_CLIENT_INFO structures for use with enumeration functions.
helpviewer_keywords: ["*LPDHCP_CLIENT_INFO_ARRAY","DHCP_CLIENT_INFO_ARRAY","DHCP_CLIENT_INFO_ARRAY structure [DHCP]","LPDHCP_CLIENT_INFO_ARRAY","LPDHCP_CLIENT_INFO_ARRAY structure pointer [DHCP]","dhcp.dhcp_client_info_array","dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY","dhcpsapi/_DHCP_CLIENT_INFO_ARRAY"]
old-location: dhcp\dhcp_client_info_array.htm
tech.root: DHCP
ms.assetid: 32bb0664-5227-4c84-a2d8-c3b348ae451c
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO_ARRAY, DHCP_CLIENT_INFO_ARRAY, DHCP_CLIENT_INFO_ARRAY structure [DHCP], LPDHCP_CLIENT_INFO_ARRAY, LPDHCP_CLIENT_INFO_ARRAY structure pointer [DHCP], dhcp.dhcp_client_info_array, dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY, dhcpsapi/_DHCP_CLIENT_INFO_ARRAY'
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
req.typenames: DHCP_CLIENT_INFO_ARRAY, *LPDHCP_CLIENT_INFO_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_INFO_ARRAY
 - dhcpsapi/_DHCP_CLIENT_INFO_ARRAY
 - LPDHCP_CLIENT_INFO_ARRAY
 - dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY
 - DHCP_CLIENT_INFO_ARRAY
 - dhcpsapi/DHCP_CLIENT_INFO_ARRAY
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
 - DHCP_CLIENT_INFO_ARRAY
---

# DHCP_CLIENT_INFO_ARRAY structure


## -description

The <b>DHCP_CLIENT_INFO_ARRAY</b> structure defines an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a> structures for use with enumeration functions.

## -struct-fields

### -field NumElements

Specifies the number of elements present in <b>Clients</b>.

### -field Clients

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a> structures that contain information on specific DHCP subnet clients.).

### -field Clients.size_is

### -field Clients.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info">DHCP_CLIENT_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetclients">DhcpEnumSubnetClients</a>