---
UID: NS:dhcpsapi._DHCP_FILTER_ADD_INFOV4
title: "_DHCP_FILTER_ADD_INFOV4"
author: windows-driver-content
description: Contains information regarding the link-layer filter to be added to the allow and deny filter list.
old-location: dhcp\dhcp_filter_add_info.htm
old-project: DHCP
ms.assetid: eed7fffa-a48c-4ebc-ba3a-a118d2b0e20b
ms.author: windowsdriverdev
ms.date: 4/7/2018
ms.keywords: "*LPDHCP_FILTER_ADD_INFO, DHCP_FILTER_ADD_INFO, DHCP_FILTER_ADD_INFO structure [DHCP], PDHCP_FILTER_ADD_INFO, PDHCP_FILTER_ADD_INFO structure pointer [DHCP], _DHCP_FILTER_ADD_INFOV4, dhcp.dhcp_filter_add_info, dhcpsapi/DHCP_FILTER_ADD_INFO, dhcpsapi/PDHCP_FILTER_ADD_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: DHCP_FILTER_ADD_INFO, *LPDHCP_FILTER_ADD_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_FILTER_ADD_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_FILTER_ADD_INFOV4 structure


## -description


The <b>DHCP_FILTER_ADD_INFO</b> structure contains information regarding the link-layer filter to be added to the allow and deny filter list.


## -struct-fields




### -field AddrPatt


<a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a> structure that contains the address/pattern-related information of the link-layer filter.


### -field Comment

Pointer to a Unicode string that contains a text comment for the filter.


### -field ListType


<a href="https://msdn.microsoft.com/369b705c-2322-4be7-8550-41a42318204b">DHCP_FILTER_LIST_TYPE</a> enumeration value that specifies the list type to which the filter is to be added.


## -see-also




<a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a>



<a href="https://msdn.microsoft.com/369b705c-2322-4be7-8550-41a42318204b">DHCP_FILTER_LIST_TYPE</a>
 

 

