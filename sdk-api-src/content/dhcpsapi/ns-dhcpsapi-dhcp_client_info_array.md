---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_ARRAY
title: DHCP_CLIENT_INFO_ARRAY (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_CLIENT_INFO_ARRAY structure defines an array of DHCP_CLIENT_INFO structures for use with enumeration functions.
old-location: dhcp\dhcp_client_info_array.htm
tech.root: DHCP
ms.assetid: 32bb0664-5227-4c84-a2d8-c3b348ae451c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_CLIENT_INFO_ARRAY, DHCP_CLIENT_INFO_ARRAY, DHCP_CLIENT_INFO_ARRAY structure [DHCP], LPDHCP_CLIENT_INFO_ARRAY, LPDHCP_CLIENT_INFO_ARRAY structure pointer [DHCP], dhcp.dhcp_client_info_array, dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY, dhcpsapi/_DHCP_CLIENT_INFO_ARRAY"
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
 - DHCP_CLIENT_INFO_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCP_CLIENT_INFO_ARRAY, *LPDHCP_CLIENT_INFO_ARRAY
req.redist: 
---

# DHCP_CLIENT_INFO_ARRAY structure


## -description


The <b>DHCP_CLIENT_INFO_ARRAY</b> structure defines an array of <a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a> structures for use with enumeration functions.


## -struct-fields




### -field NumElements

Specifies the number of elements present in <b>Clients</b>.


### -field Clients

Pointer to a list of <a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a> structures that contain information on specific DHCP subnet clients.).


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/cc841dac-85d4-4250-a868-95c41731fe45">DHCP_CLIENT_INFO</a>



<a href="https://msdn.microsoft.com/04ef441e-0638-4ee7-a6a6-a35ab5cf7a44">DhcpEnumSubnetClients</a>
 

 

