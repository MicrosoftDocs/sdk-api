---
UID: NF:dhcpsapi.DhcpGetSuperScopeInfoV4
title: DhcpGetSuperScopeInfoV4 function (dhcpsapi.h)
description: Returns information on the superscope of a DHCP server.
helpviewer_keywords: ["DhcpGetSuperScopeInfoV4","DhcpGetSuperScopeInfoV4 function [DHCP]","dhcp.dhcpgetsuperscopeinfov4","dhcpsapi/DhcpGetSuperScopeInfoV4"]
old-location: dhcp\dhcpgetsuperscopeinfov4.htm
tech.root: DHCP
ms.assetid: f40c77b8-c8ad-432d-8a9e-6719630826ef
ms.date: 12/05/2018
ms.keywords: DhcpGetSuperScopeInfoV4, DhcpGetSuperScopeInfoV4 function [DHCP], dhcp.dhcpgetsuperscopeinfov4, dhcpsapi/DhcpGetSuperScopeInfoV4
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpGetSuperScopeInfoV4
 - dhcpsapi/DhcpGetSuperScopeInfoV4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpGetSuperScopeInfoV4
---

# DhcpGetSuperScopeInfoV4 function


## -description

The <b>DhcpGetSuperScopeInfoV4</b> function returns information on the superscope of a DHCP server.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SuperScopeTable [out]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_super_scope_table">DHCP_SUPER_SCOPE_TABLE</a> structure that contains the returned information for the superscope of the supplied DHCP server.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
</table>

## -remarks

A superscope is the set of all subnets defined on a DHCP server, and hence all scopes along with the IP address ranges each serves. Taken altogether, a superscope provides a complete set of all IP addresses served by the DHCP server. The superscope table provides the IP addresses associated with each subnet. To obtain the IP ranges served by each, <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetsubnetinfo">DhcpGetSubnetInfo</a> should be called on the IP address provided in each <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_super_scope_table_entry">DHCP_SUPER_SCOPE_TABLE_ENTRY</a> structure of the table.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_super_scope_table">DHCP_SUPER_SCOPE_TABLE</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetsubnetinfo">DhcpGetSubnetInfo</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetsuperscopev4">DhcpSetSuperScopeV4</a>