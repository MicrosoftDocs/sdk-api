---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
title: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 (dhcpsapi.h)
description: Defines an array of subnet element data. Element data in the V4 structure contains client type information.
helpviewer_keywords: ["*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4","DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4","DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure [DHCP]","LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4","LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure pointer [DHCP]","dhcp.dhcp_subnet_element_info_array_v4","dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4","dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4"]
old-location: dhcp\dhcp_subnet_element_info_array_v4.htm
tech.root: DHCP
ms.assetid: e70581b4-879b-450f-a99b-754145f4bee8
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure [DHCP], LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure pointer [DHCP], dhcp.dhcp_subnet_element_info_array_v4, dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4'
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
req.typenames: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, *LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
 - dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
 - LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
 - dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
 - dhcpsapi/DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
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
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
---

# DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure


## -description

The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4</b> structure defines an array of subnet element data. Element data in the V4 structure contains client type information.

## -struct-fields

### -field NumElements

Specifies the number of elements in <b>Elements</b>.

### -field Elements

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v4">DHCP_SUBNET_ELEMENT_DATA_V4</a> structures that contain the data for the corresponding subnet elements.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data_v4">DHCP_SUBNET_ELEMENT_DATA_V4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetelementsv4">DhcpEnumSubnetElementsV4</a>