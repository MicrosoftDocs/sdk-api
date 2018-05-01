---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
title: "_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5"
author: windows-driver-content
description: The DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure defines an array of subnet element data. Element data in the V5 structure is BOOTP specific.
old-location: dhcp\dhcp_subnet_element_info_array_v5.htm
old-project: DHCP
ms.assetid: 427683d5-e285-49b7-a68b-3c75b8b8ce23
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure [DHCP], LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure pointer [DHCP], _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, dhcp.dhcp_subnet_element_info_array_v5, dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5, *LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5 structure


## -description


The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY_V5</b> structure defines an array of subnet element data. Element data in the V5 structure is BOOTP specific.


## -struct-fields




### -field NumElements

Specifies the number of elements in <b>Elements</b>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/ea6df1bc-2d15-4a09-8100-ee17d3de34d9">DHCP_SUBNET_ELEMENT_DATA_V5</a> structures that contain the data for the corresponding subnet elements.


## -see-also




<a href="https://msdn.microsoft.com/ea6df1bc-2d15-4a09-8100-ee17d3de34d9">DHCP_SUBNET_ELEMENT_DATA_V5</a>



<a href="https://msdn.microsoft.com/d6fd543c-5036-469e-9e48-02573c7dcb9f">DhcpEnumSubnetElementsV5</a>
 

 

