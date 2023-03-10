---
UID: NF:dhcpsapi.DhcpDeleteClassV6
title: DhcpDeleteClassV6 function (dhcpsapi.h)
description: Deletes a DHCP class from the DHCPv6 server.
helpviewer_keywords: ["DhcpDeleteClassV6","DhcpDeleteClassV6 function [DHCP]","dhcp.dhcpdeleteclassv6","dhcpsapi/DhcpDeleteClassV6"]
old-location: dhcp\dhcpdeleteclassv6.htm
tech.root: DHCP
ms.assetid: b818ed6f-16a3-4259-be40-001875809c78
ms.date: 12/05/2018
ms.keywords: DhcpDeleteClassV6, DhcpDeleteClassV6 function [DHCP], dhcp.dhcpdeleteclassv6, dhcpsapi/DhcpDeleteClassV6
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
 - DhcpDeleteClassV6
 - dhcpsapi/DhcpDeleteClassV6
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
 - DhcpDeleteClassV6
---

# DhcpDeleteClassV6 function


## -description

The <b>DhcpDeleteClassV6</b> function deletes a DHCP class from the DHCPv6 server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that contains the IPv6 address of the DHCPv6 server. This string is used as a handle for resolving RPC API calls.

### -param ReservedMustBeZero [in]

Reserved. This parameter must be set to 0.

### -param ClassName [in]

Unicode string that specifies the name of the DHCPv6 class to delete.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The class name could not be found in the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_DELETE_BUILTIN_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The class is a built-in class and cannot be deleted.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateclassv6">DhcpCreateClassV6</a>