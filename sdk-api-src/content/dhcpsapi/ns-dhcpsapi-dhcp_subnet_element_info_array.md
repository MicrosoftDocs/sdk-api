---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_INFO_ARRAY
title: DHCP_SUBNET_ELEMENT_INFO_ARRAY (dhcpsapi.h)
description: Defines an array of subnet element data.
helpviewer_keywords: ["*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY","DHCP_SUBNET_ELEMENT_INFO_ARRAY","DHCP_SUBNET_ELEMENT_INFO_ARRAY structure [DHCP]","LPDHCP_SUBNET_ELEMENT_INFO_ARRAY","LPDHCP_SUBNET_ELEMENT_INFO_ARRAY structure pointer [DHCP]","dhcp.dhcp_subnet_element_info_array","dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY","dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY"]
old-location: dhcp\dhcp_subnet_element_info_array.htm
tech.root: DHCP
ms.assetid: 50fbcae7-ea0c-4b46-a042-d463ab496e12
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY, DHCP_SUBNET_ELEMENT_INFO_ARRAY, DHCP_SUBNET_ELEMENT_INFO_ARRAY structure [DHCP], LPDHCP_SUBNET_ELEMENT_INFO_ARRAY, LPDHCP_SUBNET_ELEMENT_INFO_ARRAY structure pointer [DHCP], dhcp.dhcp_subnet_element_info_array, dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY, dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY'
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
req.typenames: DHCP_SUBNET_ELEMENT_INFO_ARRAY, *LPDHCP_SUBNET_ELEMENT_INFO_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUBNET_ELEMENT_INFO_ARRAY
 - dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY
 - LPDHCP_SUBNET_ELEMENT_INFO_ARRAY
 - dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY
 - dhcpsapi/DHCP_SUBNET_ELEMENT_INFO_ARRAY
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
 - DHCP_SUBNET_ELEMENT_INFO_ARRAY
---

# DHCP_SUBNET_ELEMENT_INFO_ARRAY structure


## -description

The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY</b> structure defines an array of subnet element data.

## -struct-fields

### -field NumElements

Specifies the number of elements in <b>Elements</b>.

### -field Elements

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data">DHCP_SUBNET_ELEMENT_DATA</a> structures that contain the data for the corresponding subnet elements.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_subnet_element_data">DHCP_SUBNET_ELEMENT_DATA</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnetelements">DhcpEnumSubnetElements</a>