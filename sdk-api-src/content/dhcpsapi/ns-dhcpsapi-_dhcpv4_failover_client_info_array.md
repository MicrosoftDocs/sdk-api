---
UID: NS:dhcpsapi._DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
title: "_DHCPV4_FAILOVER_CLIENT_INFO_ARRAY"
author: windows-sdk-content
description: The DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure defines an array of DHCP server scope statistics that are part of a failover relationship.
old-location: dhcp\dhcpv4_failover_client_info_array.htm
old-project: dhcp
ms.assetid: D988F420-28F0-4F13-B2A1-CFD9A71669A4
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*LPDHCPV4_FAILOVER_CLIENT_INFO_ARRAY, DHCPV4_FAILOVER_CLIENT_INFO_ARRAY, DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure [DHCP], PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY, PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure pointer [DHCP], _DHCPV4_FAILOVER_CLIENT_INFO_ARRAY, dhcp.dhcpv4_failover_client_info_array, dhcpsapi/DHCPV4_FAILOVER_CLIENT_INFO_ARRAY, dhcpsapi/PDHCPV4_FAILOVER_CLIENT_INFO_ARRAY"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DHCPV4_FAILOVER_CLIENT_INFO_ARRAY, *LPDHCPV4_FAILOVER_CLIENT_INFO_ARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCPV4_FAILOVER_CLIENT_INFO_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCPV4_FAILOVER_CLIENT_INFO_ARRAY structure


## -description


The <b>DHCPV4_FAILOVER_CLIENT_INFO_ARRAY</b> structure defines an array of DHCP server scope statistics that are part of a failover relationship.


## -struct-fields




### -field NumElements

Integer that specifies the number of DHCP server scope statistics in <b>Clients</b>.


### -field Clients

Pointer to an array of <a href="https://msdn.microsoft.com/46e4fb62-5b8e-44f8-b3a0-92535ca690f0">DHCPV4_FAILOVER_CLIENT_INFO</a>  structures.


### -field Clients.size_is

 


### -field Clients.size_is.NumElements

 



