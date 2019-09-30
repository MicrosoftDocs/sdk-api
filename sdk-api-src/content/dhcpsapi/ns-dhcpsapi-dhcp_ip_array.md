---
UID: NS:dhcpsapi._DHCP_IP_ARRAY
title: DHCP_IP_ARRAY (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_IP_ARRAY structure defines an array of IP addresses.
old-location: dhcp\dhcp_ip_array.htm
tech.root: DHCP
ms.assetid: 84f42e55-8364-4119-83e4-c03699a9aa0a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_IP_ARRAY, DHCP_IP_ARRAY, DHCP_IP_ARRAY structure [DHCP], LPDHCP_IP_ARRAY, LPDHCP_IP_ARRAY structure pointer [DHCP], dhcp.dhcp_ip_array, dhcpsapi/LPDHCP_IP_ARRAY, dhcpsapi/_DHCP_IP_ARRAY"
ms.topic: struct
f1_keywords: 
 - "dhcpsapi/DHCP_IP_ARRAY"
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
 - DHCP_IP_ARRAY
targetos: Windows
req.typenames: DHCP_IP_ARRAY, *LPDHCP_IP_ARRAY
req.redist: 
ms.custom: 19H1
---

# DHCP_IP_ARRAY structure


## -description


The <b>DHCP_IP_ARRAY</b> structure defines an array of IP addresses.


## -struct-fields




### -field NumElements

Specifies the number of IP addresses in <b>Elements</b>.


### -field Elements

Pointer to a list of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> values.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpenumsubnets">DhcpEnumSubnets</a>
 

 

