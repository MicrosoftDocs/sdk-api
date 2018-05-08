---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_PB_ARRAY
title: "_DHCP_CLIENT_INFO_PB_ARRAY"
author: windows-driver-content
description: The DHCP_CLIENT_INFO_PB_ARRAY structure defines an array of DHCPv4 client information elements.
old-location: dhcp\dhcp_client_info_pb_array.htm
old-project: DHCP
ms.assetid: a5106bba-0b84-4a89-b586-e4d115bf4cfe
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: "*LPDHCP_CLIENT_INFO_PB_ARRAY, DHCP_CLIENT_INFO_PB_ARRAY, DHCP_CLIENT_INFO_PB_ARRAY structure [DHCP], LPDHCP_CLIENT_INFO_PB_ARRAY, LPDHCP_CLIENT_INFO_PB_ARRAY structure pointer [DHCP], _DHCP_CLIENT_INFO_PB_ARRAY, dhcp.dhcp_client_info_pb_array, dhcpsapi/DHCP_CLIENT_INFO_PB_ARRAY, dhcpsapi/LPDHCP_CLIENT_INFO_PB_ARRAY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCP_CLIENT_INFO_PB_ARRAY, *LPDHCP_CLIENT_INFO_PB_ARRAY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dhcpsapi.h
api_name:
-	DHCP_CLIENT_INFO_PB_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_INFO_PB_ARRAY structure


## -description


The <b>DHCP_CLIENT_INFO_PB_ARRAY</b> structure defines an array of DHCPv4 client information elements.


## -struct-fields




### -field NumElements

Integer that contains the number of DHCPv4 clients in <b>Clients</b>.


### -field Clients

Pointer to an array of <a href="https://msdn.microsoft.com/3ee224fb-650f-4468-848b-960424202ac3">DHCP_CLIENT_INFO_PB</a> structures that contain DHCPv4 client information.


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/f6c6113b-fabd-4094-a160-8da7a139bdc4">DhcpV4EnumSubnetClients</a>
 

 

