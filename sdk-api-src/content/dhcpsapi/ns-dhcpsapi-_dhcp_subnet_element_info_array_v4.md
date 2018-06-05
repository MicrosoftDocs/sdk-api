---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
title: "_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4"
author: windows-sdk-content
description: Defines an array of subnet element data. Element data in the V4 structure contains client type information.
old-location: dhcp\dhcp_subnet_element_info_array_v4.htm
old-project: DHCP
ms.assetid: e70581b4-879b-450f-a99b-754145f4bee8
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure [DHCP], LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure pointer [DHCP], _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, dhcp.dhcp_subnet_element_info_array_v4, dhcpsapi/LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, dhcpsapi/_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4, *LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4 structure


## -description


The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY_V4</b> structure defines an array of subnet element data. Element data in the V4 structure contains client type information.


## -struct-fields




### -field NumElements

Specifies the number of elements in <b>Elements</b>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/d17725da-516b-4be6-839e-9876653e63c4">DHCP_SUBNET_ELEMENT_DATA_V4</a> structures that contain the data for the corresponding subnet elements.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/d17725da-516b-4be6-839e-9876653e63c4">DHCP_SUBNET_ELEMENT_DATA_V4</a>



<a href="https://msdn.microsoft.com/561a7aac-eed9-4a80-a4a4-f3a7727ae92a">DhcpEnumSubnetElementsV4</a>
 

 

