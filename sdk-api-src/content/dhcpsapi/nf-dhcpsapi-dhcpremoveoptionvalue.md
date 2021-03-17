---
UID: NF:dhcpsapi.DhcpRemoveOptionValue
title: DhcpRemoveOptionValue function (dhcpsapi.h)
description: Removes the option value for a specific option on the DHCP4 server for the default user class and vendor class, for the specified scope.
helpviewer_keywords: ["DhcpRemoveOptionValue","DhcpRemoveOptionValue function [DHCP]","dhcp.dhcpremoveoptionvalue","dhcpsapi/DhcpRemoveOptionValue"]
old-location: dhcp\dhcpremoveoptionvalue.htm
tech.root: DHCP
ms.assetid: e370760c-d392-4e2e-a95c-7213ce593f77
ms.date: 12/05/2018
ms.keywords: DhcpRemoveOptionValue, DhcpRemoveOptionValue function [DHCP], dhcp.dhcpremoveoptionvalue, dhcpsapi/DhcpRemoveOptionValue
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
 - DhcpRemoveOptionValue
 - dhcpsapi/DhcpRemoveOptionValue
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
 - DhcpRemoveOptionValue
---

# DhcpRemoveOptionValue function


## -description

The <b>DhcpRemoveOptionValue</b> function removes the option value for a specific option on the DHCP4 server for the default user class and vendor class, for the specified scope.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param OptionID [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_OPTION_ID</a> value that contains the code uniquely identifying the specific option to remove from the DHCP server.

### -param ScopeInfo [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a> structure that contains information describing the specific scope (default, server, scope, or IPv4 reservation level) from which to remove the option value.

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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_OPTION_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified option definition could not be found in the DHCP server database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified IPv4 subnet is not defined on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_NOT_RESERVED_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP client is not a reserved client.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info">DHCP_OPTION_SCOPE_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpremoveoptionv5">DhcpRemoveOptionValueV5</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetoptionvalue">DhcpSetOptionValue</a>