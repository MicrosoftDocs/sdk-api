---
UID: NS:dhcpsapi._DHCP_OPTION_SCOPE_INFO6
title: "_DHCP_OPTION_SCOPE_INFO6"
author: windows-sdk-content
description: Defines the data associated with a DHCP option scope.
old-location: dhcp\dhcp_option_scope_info6.htm
tech.root: DHCP
ms.assetid: d5c0cff9-7164-4f14-a0a9-58311390ebd9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_OPTION_SCOPE_INFO6, DHCP_OPTION_SCOPE_INFO6, DHCP_OPTION_SCOPE_INFO6 structure [DHCP], PDHCP_OPTION_SCOPE_INFO6, PDHCP_OPTION_SCOPE_INFO6 structure pointer [DHCP], _DHCP_OPTION_SCOPE_INFO6, dhcp.dhcp_option_scope_info6, dhcpsapi/DHCP_OPTION_SCOPE_INFO6, dhcpsapi/PDHCP_OPTION_SCOPE_INFO6"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DHCP_OPTION_SCOPE_INFO6
product: Windows
targetos: Windows
req.typenames: DHCP_OPTION_SCOPE_INFO6, *LPDHCP_OPTION_SCOPE_INFO6
req.redist: 
---

# _DHCP_OPTION_SCOPE_INFO6 structure


## -description


The DHCP_OPTION_SCOPE_INFO6 structure defines the data associated with a DHCP option scope.


## -struct-fields




### -field ScopeType


<a href="https://msdn.microsoft.com/dc6811ca-571e-4d63-ac30-8a9038cb28af">DHCP_OPTION_SCOPE_TYPE6</a> enumeration value that indicates the type of the DHCP option. This value is used as the selector for the union arms listed in the following fields.


### -field ScopeInfo.SubnetScopeInfo.case

 


### -field ScopeInfo.SubnetScopeInfo.case.DhcpScopeOptions6

 


### -field ScopeInfo.ReservedScopeInfo.case

 


### -field ScopeInfo.ReservedScopeInfo.case.DhcpReservedOptions6

 


### -field ScopeInfo.switch_is

 


### -field ScopeInfo.switch_is.ScopeType

 


### -field ScopeInfo.switch_type

 


### -field ScopeInfo.switch_type.DHCP_OPTION_SCOPE_TYPE6

 


### -field ScopeInfo


### -field ScopeInfo.DefaultScopeInfo

Pointer to data the specifies the default scope information. This must be set to null.


### -field ScopeInfo.SubnetScopeInfo

IPv6 mask for the subnet that defines the DHCP scope.


### -field ScopeInfo.ReservedScopeInfo

DHCP_RESERVED_SCOPE6 structure that contains the reserved DHCP scope information.


### -field _DHCP_OPTION_SCOPE_UNION6

 




## -see-also




<a href="https://msdn.microsoft.com/dc6811ca-571e-4d63-ac30-8a9038cb28af">DHCP_OPTION_SCOPE_TYPE6</a>
 

 

