---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
title: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 (dhcpsapi.h)
description: The DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure defines an array of subnet element data. Element data in the V5 structure is BOOTP specific.
helpviewer_keywords: ["*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5","DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5","DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure [DHCP]","LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5","LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure pointer [DHCP]","dhcp.dhcp_subnet_element_info_array_v5","dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5","dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5"]
old-location: dhcp\dhcp_subnet_element_info_array_v5.htm
tech.root: DHCP
ms.assetid: 427683d5-e285-49b7-a68b-3c75b8b8ce23
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure [DHCP], LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure pointer [DHCP], dhcp.dhcp_subnet_element_info_array_v5, dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5'
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
req.typenames: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, *LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
 - dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
 - LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
 - dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
 - dhcpsapi/DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
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
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
---

# DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure


## -description

The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5</b> structure defines an array of subnet element data. Element data in the V5 structure is BOOTP specific.

## -struct-fields

### -field NumElements

Specifies the number of elements in <b>Elements</b>.

### -field Elements

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v5">DHCP_SUBNET_ELEMENT_DATA_V5</a> structures that contain the data for the corresponding subnet elements.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v5">DHCP_SUBNET_ELEMENT_DATA_V5</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetelementsv5">DhcpEnumSubnetElementsV5</a>