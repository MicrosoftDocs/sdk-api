---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
title: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 (dhcpsapi.h)
description: Contains data that defines an array of DHCP_SUBNET_ELEMENT_DATA_V6 IPv6 prefix elements.
helpviewer_keywords: ["*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6","DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6","DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure [DHCP]","PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6","PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure pointer [DHCP]","dhcp.dhcp_subnet_element_info_array_v6","dhcpsapi/DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6","dhcpsapi/PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6"]
old-location: dhcp\dhcp_subnet_element_info_array_v6.htm
tech.root: DHCP
ms.assetid: 02e7e633-173d-46ab-b657-4763d367f325
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure [DHCP], PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure pointer [DHCP], dhcp.dhcp_subnet_element_info_array_v6, dhcpsapi/DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, dhcpsapi/PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, *LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
 - dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
 - LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
 - dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
 - dhcpsapi/DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
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
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
---

# DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure


## -description

The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6</b> structure contains data that defines an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v6">DHCP_SUBNET_ELEMENT_DATA_V6</a> IPv6 prefix elements.

## -struct-fields

### -field NumElements

A <b>DWORD</b> value containing the number of IPv6 subnet elements in the <b>Elements</b> member.

### -field Elements

Pointer to an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v6">DHCP_SUBNET_ELEMENT_DATA_V6</a> structures that contain IPv6 prefix elements.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v6">DHCP_SUBNET_ELEMENT_DATA_V6</a>