---
UID: NS:dhcpsapi._DHCP_FILTER_RECORD
title: "_DHCP_FILTER_RECORD"
author: windows-sdk-content
description: Contains information for a specific link-layer filter.
old-location: dhcp\dhcp_filter_record.htm
old-project: DHCP
ms.assetid: 5f8531fe-cc30-4baf-904b-15627d1ff750
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_FILTER_RECORD, DHCP_FILTER_RECORD, DHCP_FILTER_RECORD structure [DHCP], PDHCP_FILTER_RECORD, PDHCP_FILTER_RECORD structure pointer [DHCP], _DHCP_FILTER_RECORD, dhcp.dhcp_filter_record, dhcpsapi/DHCP_FILTER_RECORD, dhcpsapi/PDHCP_FILTER_RECORD"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DHCP_FILTER_RECORD, *LPDHCP_FILTER_RECORD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpsapi.h
api_name:
-	DHCP_FILTER_RECORD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_FILTER_RECORD structure


## -description


The <b>DHCP_FILTER_RECORD</b> structure contains information for a specific link-layer filter.


## -struct-fields




### -field AddrPatt


<a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a> structure that contains the address/pattern related information of the link-layer filter.


### -field Comment

Pointer to a null-terminated Unicode string which contains the comment associated with the address/pattern.


## -see-also




<a href="https://msdn.microsoft.com/8c645b03-9859-48e9-8974-2dbdc9cfcac6">DHCP_ADDR_PATTERN</a>
 

 

