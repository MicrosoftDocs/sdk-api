---
UID: NS:dhcpsapi._DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
title: DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY (dhcpsapi.h)
description: Contains an array of information elements for DHCPv4 clients.
helpviewer_keywords: ["*LPDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY","DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY","DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure [DHCP]","PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY","PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure pointer [DHCP]","dhcp.dhcp_client_filter_status_info_array","dhcpsapi/DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY","dhcpsapi/PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY"]
old-location: dhcp\dhcp_client_filter_status_info_array.htm
tech.root: DHCP
ms.assetid: 3145befc-9274-4719-9cd7-1f6426a86fba
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure [DHCP], PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure pointer [DHCP], dhcp.dhcp_client_filter_status_info_array, dhcpsapi/DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, dhcpsapi/PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY'
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
req.typenames: DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, *LPDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
 - dhcpsapi/_DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
 - LPDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
 - dhcpsapi/LPDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
 - DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
 - dhcpsapi/DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
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
 - DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
---

# DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure


## -description

The <b>DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY</b> structure contains an array of information elements for DHCPv4 clients.

## -struct-fields

### -field NumElements

Integer value that contains the number of DHCPv4 clients in the subsequent field Clients.

### -field Clients

Pointer to an array of  <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_filter_status_info">DHCP_CLIENT_FILTER_STATUS_INFO</a> structures that contain the DHCPv4 clients'  information.

### -field Clients.size_is

### -field Clients.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_filter_status_info">DHCP_CLIENT_FILTER_STATUS_INFO</a>