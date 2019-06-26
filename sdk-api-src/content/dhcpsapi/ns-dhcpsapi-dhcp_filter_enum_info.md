---
UID: NS:dhcpsapi._DHCP_FILTER_ENUM_INFO
title: DHCP_FILTER_ENUM_INFO (dhcpsapi.h)
author: windows-sdk-content
description: Contains information regarding the number of link-layer filter records.
old-location: dhcp\dhcp_filter_enum_info.htm
tech.root: DHCP
ms.assetid: f393987c-12dd-468c-98c6-84f4d36744b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_FILTER_ENUM_INFO, DHCP_FILTER_ENUM_INFO, DHCP_FILTER_ENUM_INFO structure [DHCP], PDHCP_FILTER_ENUM_INFO, PDHCP_FILTER_ENUM_INFO structure pointer [DHCP], dhcp.dhcp_filter_enum_info, dhcpsapi/DHCP_FILTER_ENUM_INFO, dhcpsapi/PDHCP_FILTER_ENUM_INFO"
ms.topic: struct
f1_keywords: 
 - "dhcpsapi/DHCP_FILTER_ENUM_INFO"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_FILTER_ENUM_INFO
product: Windows
targetos: Windows
req.typenames: DHCP_FILTER_ENUM_INFO, *LPDHCP_FILTER_ENUM_INFO
req.redist: 
ms.custom: 19H1
---

# DHCP_FILTER_ENUM_INFO structure


## -description


The <b>DHCP_FILTER_ENUM_INFO</b> structure contains information regarding the number of link-layer filter records.


## -struct-fields




### -field NumElements

Integer value that specifies the number of link-layer filter records contained in the array specified by pEnumRecords.


### -field pEnumRecords

Pointer to an array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_filter_record">DHCP_FILTER_RECORD</a> structures that contain link-layer filter records.


### -field pEnumRecords.size_is

 


### -field pEnumRecords.size_is.NumElements

 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_filter_record">DHCP_FILTER_RECORD</a>
 

 

