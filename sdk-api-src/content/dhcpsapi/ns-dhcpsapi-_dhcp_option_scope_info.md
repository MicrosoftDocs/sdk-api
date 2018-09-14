---
UID: NS:dhcpsapi._DHCP_OPTION_SCOPE_INFO
title: "_DHCP_OPTION_SCOPE_INFO"
author: windows-sdk-content
description: The DHCP_OPTION_SCOPE_INFO structure defines information about the options provided for a certain DHCP scope.
old-location: dhcp\dhcp_option_scope_info.htm
tech.root: DHCP
ms.assetid: 91d4d678-f0c5-4081-9302-0d08c8994692
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPDHCP_OPTION_SCOPE_INFO, DHCP_OPTION_SCOPE_INFO, DHCP_OPTION_SCOPE_INFO structure [DHCP], LPDHCP_OPTION_SCOPE_INFO, LPDHCP_OPTION_SCOPE_INFO structure pointer [DHCP], _DHCP_OPTION_SCOPE_INFO, dhcp.dhcp_option_scope_info, dhcpsapi/LPDHCP_OPTION_SCOPE_INFO, dhcpsapi/_DHCP_OPTION_SCOPE_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
 - DHCP_OPTION_SCOPE_INFO
product: Windows
targetos: Windows
req.typenames: DHCP_OPTION_SCOPE_INFO, *LPDHCP_OPTION_SCOPE_INFO
req.redist: 
---

# _DHCP_OPTION_SCOPE_INFO structure


## -description


The <b>DHCP_OPTION_SCOPE_INFO</b> structure defines information about the options provided for a certain DHCP  scope.


## -struct-fields




### -field ScopeType


<a href="https://msdn.microsoft.com/3e49bbe4-a8d2-4e1a-b66d-a7d4b45dd670">DHCP_OPTION_SCOPE_TYPE</a> enumeration value that defines the scope type of the associated DHCP options, and indicates which of the following fields in the union will be populated.


### -field ScopeInfo.SubnetScopeInfo.case

 


### -field ScopeInfo.SubnetScopeInfo.case.DhcpSubnetOptions

 


### -field ScopeInfo.ReservedScopeInfo.case

 


### -field ScopeInfo.ReservedScopeInfo.case.DhcpReservedOptions

 


### -field ScopeInfo.MScopeInfo.case

 


### -field ScopeInfo.MScopeInfo.case.DhcpMScopeOptions

 


### -field ScopeInfo.switch_is

 


### -field ScopeInfo.switch_is.ScopeType

 


### -field ScopeInfo.switch_type

 


### -field ScopeInfo.switch_type.DHCP_OPTION_SCOPE_TYPE

 


### -field ScopeInfo


### -field ScopeInfo.DefaultScopeInfo

Pointer to a <a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a> structure that contains the default DHCP scope options. This member is not currently used.


### -field ScopeInfo.GlobalScopeInfo

Pointer to a <a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a> structure that contains the global DHCP server options.


### -field ScopeInfo.SubnetScopeInfo


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the subnet ID as a DWORD.


### -field ScopeInfo.ReservedScopeInfo


<a href="https://msdn.microsoft.com/e3b8bcc1-9cdc-499f-840a-3545ec9b46f7">DHCP_RESERVED_SCOPE</a> structure that contains a reserved IP address and its corresponding subnet ID.


### -field ScopeInfo.MScopeInfo

Pointer to a Unicode string that contains the multicast scope name (usually represented as the IP address of the multicast router).


### -field _DHCP_OPTION_SCOPE_UNION

 




## -see-also




<a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a>



<a href="https://msdn.microsoft.com/3e49bbe4-a8d2-4e1a-b66d-a7d4b45dd670">DHCP_OPTION_SCOPE_TYPE</a>



<a href="https://msdn.microsoft.com/e3b8bcc1-9cdc-499f-840a-3545ec9b46f7">DHCP_RESERVED_SCOPE</a>
 

 

