---
UID: NS:dhcpsapi._DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
title: "_DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY"
author: windows-sdk-content
description: Contains an array of information elements for DHCPv4 clients.
old-location: dhcp\dhcp_client_filter_status_info_array.htm
old-project: dhcp
ms.assetid: 3145befc-9274-4719-9cd7-1f6426a86fba
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*LPDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure [DHCP], PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure pointer [DHCP], _DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, dhcp.dhcp_client_filter_status_info_array, dhcpsapi/DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, dhcpsapi/PDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY"
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
req.typenames: DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY, *LPDHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY structure


## -description


The <b>DHCP_CLIENT_FILTER_STATUS_INFO_ARRAY</b> structure contains an array of information elements for DHCPv4 clients.




## -struct-fields




### -field NumElements

Integer value that contains the number of DHCPv4 clients in the subsequent field Clients.



### -field Clients

Pointer to an array of  <a href="https://msdn.microsoft.com/71b36ce1-e3de-4904-bbf2-8d305bae06b0">DHCP_CLIENT_FILTER_STATUS_INFO</a> structures that contain the DHCPv4 clients'  information.




### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/71b36ce1-e3de-4904-bbf2-8d305bae06b0">DHCP_CLIENT_FILTER_STATUS_INFO</a>
 

 

