---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_ARRAY_V4
title: DHCP_CLIENT_INFO_ARRAY_V4 (dhcpsapi.h)
description: Defines an array of DHCP_CLIENT_INFO_V4 structures for use with enumeration functions.
helpviewer_keywords: ["*LPDHCP_CLIENT_INFO_ARRAY_V4","DHCP_CLIENT_INFO_ARRAY_V4","DHCP_CLIENT_INFO_ARRAY_V4 structure [DHCP]","LPDHCP_CLIENT_INFO_ARRAY_V4","LPDHCP_CLIENT_INFO_ARRAY_V4 structure pointer [DHCP]","dhcp.dhcp_client_info_array_v4","dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY_V4","dhcpsapi/_DHCP_CLIENT_INFO_ARRAY_V4"]
old-location: dhcp\dhcp_client_info_array_v4.htm
tech.root: DHCP
ms.assetid: cda4bf44-0a4c-4825-ae3f-379ceae5aadb
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO_ARRAY_V4, DHCP_CLIENT_INFO_ARRAY_V4, DHCP_CLIENT_INFO_ARRAY_V4 structure [DHCP], LPDHCP_CLIENT_INFO_ARRAY_V4, LPDHCP_CLIENT_INFO_ARRAY_V4 structure pointer [DHCP], dhcp.dhcp_client_info_array_v4, dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY_V4, dhcpsapi/_DHCP_CLIENT_INFO_ARRAY_V4'
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
req.typenames: DHCP_CLIENT_INFO_ARRAY_V4, *LPDHCP_CLIENT_INFO_ARRAY_V4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_INFO_ARRAY_V4
 - dhcpsapi/_DHCP_CLIENT_INFO_ARRAY_V4
 - LPDHCP_CLIENT_INFO_ARRAY_V4
 - dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY_V4
 - DHCP_CLIENT_INFO_ARRAY_V4
 - dhcpsapi/DHCP_CLIENT_INFO_ARRAY_V4
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
 - DHCP_CLIENT_INFO_ARRAY_V4
---

# DHCP_CLIENT_INFO_ARRAY_V4 structure


## -description

The <b>DHCP_CLIENT_INFO_ARRAY_V4</b> structure defines an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a> structures for use with enumeration functions.

## -struct-fields

### -field NumElements

Specifies the number of elements present in <b>Clients</b>.

### -field Clients

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a> structures that contain information on specific DHCP subnet clients, including the dynamic address type (DHCP and/or BOOTP).

### -field Clients.size_is

### -field Clients.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a>