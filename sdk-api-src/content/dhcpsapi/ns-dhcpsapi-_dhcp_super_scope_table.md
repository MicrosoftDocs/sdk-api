---
UID: NS:dhcpsapi._DHCP_SUPER_SCOPE_TABLE
title: "_DHCP_SUPER_SCOPE_TABLE"
author: windows-sdk-content
description: Defines the superscope of a DHCP server.
old-location: dhcp\dhcp_super_scope_table.htm
old-project: DHCP
ms.assetid: ed7ad090-b13a-464b-af03-04944f018b36
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_SUPER_SCOPE_TABLE, DHCP_SUPER_SCOPE_TABLE, DHCP_SUPER_SCOPE_TABLE structure [DHCP], LPDHCP_SUPER_SCOPE_TABLE, LPDHCP_SUPER_SCOPE_TABLE structure pointer [DHCP], _DHCP_SUPER_SCOPE_TABLE, dhcp.dhcp_super_scope_table, dhcpsapi/LPDHCP_SUPER_SCOPE_TABLE, dhcpsapi/_DHCP_SUPER_SCOPE_TABLE"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DHCP_SUPER_SCOPE_TABLE, *LPDHCP_SUPER_SCOPE_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SUPER_SCOPE_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SUPER_SCOPE_TABLE structure


## -description


The <b>DHCP_SUPER_SCOPE_TABLE</b> structure defines the superscope of a DHCP server.


## -struct-fields




### -field cEntries

Specifies the number of subnets (and therefore scopes) present in the super scope.


### -field pEntries

Pointer to a list of <a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>
        structures containing the names and IP addresses of each subnet defined within the superscope.


### -field pEntries.size_is

 


### -field pEntries.size_is.cEntries

 




## -remarks



A "superscope" is the set of all subnets defined on a DHCP server, and hence all scopes along with the IP address ranges each serves. Taken altogether, it provides a complete set of all IP addresses served by the DHCP server. The superscope table will only provide the IP addresses associated with each subnet; to obtain the IP ranges served by each, <a href="https://msdn.microsoft.com/0e511993-a9c3-445b-bafc-3d66182ee32d">DhcpGetSubnetInfo</a> should be called on the IP address provided in each <a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>
        structure of the table.




## -see-also




<a href="https://msdn.microsoft.com/affaa0b0-3bd1-4d17-adec-518d2cb7e5b6">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>



<a href="https://msdn.microsoft.com/f40c77b8-c8ad-432d-8a9e-6719630826ef">DhcpGetSuperScopeInfoV4</a>
 

 

