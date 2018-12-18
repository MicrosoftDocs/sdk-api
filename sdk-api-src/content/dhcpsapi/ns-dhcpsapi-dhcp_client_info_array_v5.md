---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_ARRAY_V5
title: DHCP_CLIENT_INFO_ARRAY_V5
author: windows-sdk-content
description: Defines an array of DHCP_CLIENT_INFO_V5 structures for use with enumeration functions.
old-location: dhcp\dhcp_client_info_array_v5.htm
tech.root: DHCP
ms.assetid: 2188f187-d8d3-4579-bb04-4c4712903a91
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_CLIENT_INFO_ARRAY_V5, DHCP_CLIENT_INFO_ARRAY_V5, DHCP_CLIENT_INFO_ARRAY_V5 structure [DHCP], LPDHCP_CLIENT_INFO_ARRAY_V5, LPDHCP_CLIENT_INFO_ARRAY_V5 structure pointer [DHCP], dhcp.dhcp_client_info_array_v5, dhcpsapi/LPDHCP_CLIENT_INFO_ARRAY_V5, dhcpsapi/_DHCP_CLIENT_INFO_ARRAY_V5"
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
 - DHCP_CLIENT_INFO_ARRAY_V5
product: Windows
targetos: Windows
req.typenames: DHCP_CLIENT_INFO_ARRAY_V5, *LPDHCP_CLIENT_INFO_ARRAY_V5
req.redist: 
---

# DHCP_CLIENT_INFO_ARRAY_V5 structure


## -description


The <b>DHCP_CLIENT_INFO_ARRAY_V5</b> structure defines an array of <a href="https://msdn.microsoft.com/52003a41-8905-4f42-80e6-172c0df61ed7">DHCP_CLIENT_INFO_V5</a> structures for use with enumeration functions. 


## -struct-fields




### -field NumElements

Specifies the number of elements present in <b>Clients</b>.


### -field Clients

Pointer to a list of <a href="https://msdn.microsoft.com/52003a41-8905-4f42-80e6-172c0df61ed7">DHCP_CLIENT_INFO_V5</a> structures that contain information on specific DHCP subnet clients, including the dynamic address type (DHCP and/or BOOTP) and address state information.


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/52003a41-8905-4f42-80e6-172c0df61ed7">DHCP_CLIENT_INFO_V5</a>



<a href="https://msdn.microsoft.com/34be1d6d-10d5-4025-abc6-29857417e081">DhcpEnumSubnetClientsV5</a>
 

 

