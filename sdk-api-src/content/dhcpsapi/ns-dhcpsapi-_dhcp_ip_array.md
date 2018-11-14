---
UID: NS:dhcpsapi._DHCP_IP_ARRAY
title: "_DHCP_IP_ARRAY"
author: windows-sdk-content
description: The DHCP_IP_ARRAY structure defines an array of IP addresses.
old-location: dhcp\dhcp_ip_array.htm
tech.root: DHCP
ms.assetid: 84f42e55-8364-4119-83e4-c03699a9aa0a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPDHCP_IP_ARRAY, DHCP_IP_ARRAY, DHCP_IP_ARRAY structure [DHCP], LPDHCP_IP_ARRAY, LPDHCP_IP_ARRAY structure pointer [DHCP], _DHCP_IP_ARRAY, dhcp.dhcp_ip_array, dhcpsapi/LPDHCP_IP_ARRAY, dhcpsapi/_DHCP_IP_ARRAY"
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
product: Windows
targetos: Windows
req.typenames: DHCP_IP_ARRAY, *LPDHCP_IP_ARRAY
req.redist: 
---

# _DHCP_IP_ARRAY structure


## -description


The <b>DHCP_IP_ARRAY</b> structure defines an array of IP addresses.


## -struct-fields




### -field NumElements

Specifies the number of IP addresses in <b>Elements</b>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> values.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a>



<a href="https://msdn.microsoft.com/333381c9-66d1-44ef-911b-d543c79abefb">DhcpEnumSubnets</a>
 

 

