---
UID: NS:dhcpsapi._DHCP_SUPER_SCOPE_TABLE_ENTRY
title: "_DHCP_SUPER_SCOPE_TABLE_ENTRY"
author: windows-sdk-content
description: Defines a subnet entry within the superscope table.
old-location: dhcp\dhcp_super_scope_table_entry.htm
old-project: DHCP
ms.assetid: affaa0b0-3bd1-4d17-adec-518d2cb7e5b6
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: "*LPDHCP_SUPER_SCOPE_TABLE_ENTRY, DHCP_SUPER_SCOPE_TABLE_ENTRY, DHCP_SUPER_SCOPE_TABLE_ENTRY structure [DHCP], LPDHCP_SUPER_SCOPE_TABLE_ENTRY, LPDHCP_SUPER_SCOPE_TABLE_ENTRY structure pointer [DHCP], _DHCP_SUPER_SCOPE_TABLE_ENTRY, dhcp.dhcp_super_scope_table_entry, dhcpsapi/LPDHCP_SUPER_SCOPE_TABLE_ENTRY, dhcpsapi/_DHCP_SUPER_SCOPE_TABLE_ENTRY"
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
req.typenames: DHCP_SUPER_SCOPE_TABLE_ENTRY, *LPDHCP_SUPER_SCOPE_TABLE_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SUPER_SCOPE_TABLE_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_SUPER_SCOPE_TABLE_ENTRY structure


## -description


The <b>DHCP_SUPER_SCOPE_TABLE_ENTRY</b> structure defines a subnet entry within the superscope table.


## -struct-fields




### -field SubnetAddress


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that specifies the IP address of the gateway for the subnet. This address is used to uniquely identify a subnet served by the DHCP server.


### -field SuperScopeNumber

Specifies the index value assigned to this subnet entry, and its enumerated position within the super scope table.


### -field NextInSuperScope

Specifies the index value of the next subnet entry in the superscope table. If this value is ---, this table entry is the last one in the super scope.


### -field SuperScopeName

Unicode string that contains the name assigned to this subnet entry within the superscope.


## -see-also




<a href="https://msdn.microsoft.com/ed7ad090-b13a-464b-af03-04944f018b36">DHCP_SUPER_SCOPE_TABLE</a>
 

 

