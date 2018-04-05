---
UID: NS:dhcpsapi._DHCP_FILTER_ENUM_INFO
title: "_DHCP_FILTER_ENUM_INFO"
author: windows-driver-content
description: Contains information regarding the number of link-layer filter records.
old-location: dhcp\dhcp_filter_enum_info.htm
old-project: DHCP
ms.assetid: f393987c-12dd-468c-98c6-84f4d36744b2
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDHCP_FILTER_ENUM_INFO, DHCP_FILTER_ENUM_INFO, DHCP_FILTER_ENUM_INFO structure [DHCP], PDHCP_FILTER_ENUM_INFO, PDHCP_FILTER_ENUM_INFO structure pointer [DHCP], _DHCP_FILTER_ENUM_INFO, dhcp.dhcp_filter_enum_info, dhcpsapi/DHCP_FILTER_ENUM_INFO, dhcpsapi/PDHCP_FILTER_ENUM_INFO"
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
req.typenames: DHCP_FILTER_ENUM_INFO, *LPDHCP_FILTER_ENUM_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_FILTER_ENUM_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_FILTER_ENUM_INFO structure


## -description


The <b>DHCP_FILTER_ENUM_INFO</b> structure contains information regarding the number of link-layer filter records.


## -struct-fields




### -field NumElements

Integer value that specifies the number of link-layer filter records contained in the array specified by pEnumRecords.


### -field pEnumRecords

Pointer to an array of <a href="https://msdn.microsoft.com/5f8531fe-cc30-4baf-904b-15627d1ff750">DHCP_FILTER_RECORD</a> structures that contain link-layer filter records.


## -see-also




<a href="https://msdn.microsoft.com/5f8531fe-cc30-4baf-904b-15627d1ff750">DHCP_FILTER_RECORD</a>
 

 

