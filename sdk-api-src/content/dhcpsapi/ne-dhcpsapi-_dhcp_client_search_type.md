---
UID: NE:dhcpsapi._DHCP_CLIENT_SEARCH_TYPE
title: "_DHCP_CLIENT_SEARCH_TYPE"
author: windows-sdk-content
description: Defines the set of possible attributes used to search DHCP client information records.
old-location: dhcp\dhcp_search_info_type.htm
old-project: dhcp
ms.assetid: b635ea03-689c-4471-bff2-72fceec78440
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPDHCP_SEARCH_INFO_TYPE, DHCP_SEARCH_INFO_TYPE, DHCP_SEARCH_INFO_TYPE enumeration [DHCP], DhcpClientHardwareAddress, DhcpClientIpAddress, DhcpClientName, LPDHCP_SEARCH_INFO_TYPE, LPDHCP_SEARCH_INFO_TYPE enumeration pointer [DHCP], _DHCP_CLIENT_SEARCH_TYPE, dhcp.dhcp_search_info_type, dhcpsapi/DHCP_SEARCH_INFO_TYPE, dhcpsapi/DhcpClientHardwareAddress, dhcpsapi/DhcpClientIpAddress, dhcpsapi/DhcpClientName, dhcpsapi/LPDHCP_SEARCH_INFO_TYPE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dhcpsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DHCP_SEARCH_INFO_TYPE, *LPDHCP_SEARCH_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SEARCH_INFO_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CLIENT_SEARCH_TYPE enumeration


## -description


The <b>DHCP_SEARCH_INFO_TYPE</b> enumeration defines the set of possible attributes used to search DHCP client information records.


## -enum-fields




### -field DhcpClientIpAddress

The search will be performed against the assigned DHCP client IP address, represented as a 32-bit unsigned integer value.


### -field DhcpClientHardwareAddress

The search will be performed against the MAC address of the DHCP client network interface device, represented as a <a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_BINARY_DATA</a> structure.


### -field DhcpClientName

The search will be performed against the DHCP client's network name, represented as a Unicode string.


## -see-also




<a href="https://msdn.microsoft.com/0afdddb4-12f9-4c0b-937a-2cc311c126b4">DHCP_BINARY_DATA</a>



<a href="https://msdn.microsoft.com/3c6f85d7-c156-4379-bad9-0705698f12e5">DHCP_SEARCH_INFO</a>
 

 

