---
UID: NS:dhcpsapi._DHCP_SUPER_SCOPE_TABLE
title: DHCP_SUPER_SCOPE_TABLE (dhcpsapi.h)
description: Defines the superscope of a DHCP server.
helpviewer_keywords: ["*LPDHCP_SUPER_SCOPE_TABLE","DHCP_SUPER_SCOPE_TABLE","DHCP_SUPER_SCOPE_TABLE structure [DHCP]","LPDHCP_SUPER_SCOPE_TABLE","LPDHCP_SUPER_SCOPE_TABLE structure pointer [DHCP]","dhcp.dhcp_super_scope_table","dhcpsapi/LPDHCP_SUPER_SCOPE_TABLE","dhcpsapi/_DHCP_SUPER_SCOPE_TABLE"]
old-location: dhcp\dhcp_super_scope_table.htm
tech.root: DHCP
ms.assetid: ed7ad090-b13a-464b-af03-04944f018b36
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_SUPER_SCOPE_TABLE, DHCP_SUPER_SCOPE_TABLE, DHCP_SUPER_SCOPE_TABLE structure [DHCP], LPDHCP_SUPER_SCOPE_TABLE, LPDHCP_SUPER_SCOPE_TABLE structure pointer [DHCP], dhcp.dhcp_super_scope_table, dhcpsapi/LPDHCP_SUPER_SCOPE_TABLE, dhcpsapi/_DHCP_SUPER_SCOPE_TABLE'
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
targetos: Windows
req.typenames: DHCP_SUPER_SCOPE_TABLE, *LPDHCP_SUPER_SCOPE_TABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_SUPER_SCOPE_TABLE
 - dhcpsapi/_DHCP_SUPER_SCOPE_TABLE
 - LPDHCP_SUPER_SCOPE_TABLE
 - dhcpsapi/LPDHCP_SUPER_SCOPE_TABLE
 - DHCP_SUPER_SCOPE_TABLE
 - dhcpsapi/DHCP_SUPER_SCOPE_TABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_SUPER_SCOPE_TABLE
---

# DHCP_SUPER_SCOPE_TABLE structure


## -description

The <b>DHCP_SUPER_SCOPE_TABLE</b> structure defines the superscope of a DHCP server.

## -struct-fields

### -field cEntries

Specifies the number of subnets (and therefore scopes) present in the super scope.

### -field pEntries

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_super_scope_table_entry">DHCP_SUPER_SCOPE_TABLE_ENTRY</a> structures containing the names and IP addresses of each subnet defined within the superscope.

### -field pEntries.size_is

### -field pEntries.size_is.cEntries

## -remarks

A "superscope" is the set of all subnets defined on a DHCP server, and hence all scopes along with the IP address ranges each serves. Taken altogether, it provides a complete set of all IP addresses served by the DHCP server. The superscope table will only provide the IP addresses associated with each subnet; to obtain the IP ranges served by each, <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetsubnetinfo">DhcpGetSubnetInfo</a> should be called on the IP address provided in each <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_super_scope_table_entry">DHCP_SUPER_SCOPE_TABLE_ENTRY</a> structure of the table.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_super_scope_table_entry">DHCP_SUPER_SCOPE_TABLE_ENTRY</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetsuperscopeinfov4">DhcpGetSuperScopeInfoV4</a>