---
UID: NS:dhcpsapi._DHCP_CLIENT_INFO_PB_ARRAY
title: DHCP_CLIENT_INFO_PB_ARRAY (dhcpsapi.h)
description: The DHCP_CLIENT_INFO_PB_ARRAY structure defines an array of DHCPv4 client information elements.helpviewer_keywords: ["*LPDHCP_CLIENT_INFO_PB_ARRAY","DHCP_CLIENT_INFO_PB_ARRAY","DHCP_CLIENT_INFO_PB_ARRAY structure [DHCP]","LPDHCP_CLIENT_INFO_PB_ARRAY","LPDHCP_CLIENT_INFO_PB_ARRAY structure pointer [DHCP]","dhcp.dhcp_client_info_pb_array","dhcpsapi/DHCP_CLIENT_INFO_PB_ARRAY","dhcpsapi/LPDHCP_CLIENT_INFO_PB_ARRAY"]
old-location: dhcp\dhcp_client_info_pb_array.htm
tech.root: DHCP
ms.assetid: a5106bba-0b84-4a89-b586-e4d115bf4cfe
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_CLIENT_INFO_PB_ARRAY, DHCP_CLIENT_INFO_PB_ARRAY, DHCP_CLIENT_INFO_PB_ARRAY structure [DHCP], LPDHCP_CLIENT_INFO_PB_ARRAY, LPDHCP_CLIENT_INFO_PB_ARRAY structure pointer [DHCP], dhcp.dhcp_client_info_pb_array, dhcpsapi/DHCP_CLIENT_INFO_PB_ARRAY, dhcpsapi/LPDHCP_CLIENT_INFO_PB_ARRAY'
f1_keywords:
- dhcpsapi/DHCP_CLIENT_INFO_PB_ARRAY
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dhcpsapi.h
api_name:
- DHCP_CLIENT_INFO_PB_ARRAY
targetos: Windows
req.typenames: DHCP_CLIENT_INFO_PB_ARRAY, *LPDHCP_CLIENT_INFO_PB_ARRAY
req.redist: 
ms.custom: 19H1
---

# DHCP_CLIENT_INFO_PB_ARRAY structure


## -description


The <b>DHCP_CLIENT_INFO_PB_ARRAY</b> structure defines an array of DHCPv4 client information elements.


## -struct-fields




### -field NumElements

Integer that contains the number of DHCPv4 clients in <b>Clients</b>.


### -field Clients

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_pb">DHCP_CLIENT_INFO_PB</a> structures that contain DHCPv4 client information.


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4enumsubnetclients">DhcpV4EnumSubnetClients</a>
 

 

