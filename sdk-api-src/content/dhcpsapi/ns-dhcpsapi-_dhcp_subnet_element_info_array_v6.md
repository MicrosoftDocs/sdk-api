---
UID: NS:dhcpsapi._DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
title: "_DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6"
author: windows-sdk-content
description: Contains data that defines an array of DHCP_SUBNET_ELEMENT_DATA_V6 IPv6 prefix elements.
old-location: dhcp\dhcp_subnet_element_info_array_v6.htm
old-project: DHCP
ms.assetid: 02e7e633-173d-46ab-b657-4763d367f325
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure [DHCP], PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure pointer [DHCP], _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, dhcp.dhcp_subnet_element_info_array_v6, dhcpsapi/DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, dhcpsapi/PDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6"
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
req.typenames: DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6, *LPDHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6 structure


## -description


The <b>DHCP_SUBNET_ELEMENT_INFO_ARRAY_V6</b> structure contains data that defines an array of <a href="https://msdn.microsoft.com/de5fa8c5-5cd7-4358-bacd-f27f4b7f3761">DHCP_SUBNET_ELEMENT_DATA_V6</a> IPv6 prefix elements.


## -struct-fields




### -field NumElements

A <b>DWORD</b> value containing the number of IPv6 subnet elements in the <b>Elements</b> member.


### -field Elements

Pointer to an array of <a href="https://msdn.microsoft.com/de5fa8c5-5cd7-4358-bacd-f27f4b7f3761">DHCP_SUBNET_ELEMENT_DATA_V6</a> structures that contain IPv6 prefix elements.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/de5fa8c5-5cd7-4358-bacd-f27f4b7f3761">DHCP_SUBNET_ELEMENT_DATA_V6</a>
 

 

