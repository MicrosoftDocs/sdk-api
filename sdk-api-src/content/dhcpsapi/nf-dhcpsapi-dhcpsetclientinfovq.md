---
UID: NF:dhcpsapi.DhcpSetClientInfoVQ
title: DhcpSetClientInfoVQ function (dhcpsapi.h)
description: Sets or modifies an existing DHCP client lease record in the DHCP server record database.
helpviewer_keywords: ["DhcpSetClientInfoVQ","DhcpSetClientInfoVQ function [DHCP]","dhcp.dhcpsetclientinfovq","dhcpsapi/DhcpSetClientInfoVQ"]
old-location: dhcp\dhcpsetclientinfovq.htm
tech.root: DHCP
ms.assetid: c12ae8f5-8629-494f-905c-cbae57dcf3f1
ms.date: 12/05/2018
ms.keywords: DhcpSetClientInfoVQ, DhcpSetClientInfoVQ function [DHCP], dhcp.dhcpsetclientinfovq, dhcpsapi/DhcpSetClientInfoVQ
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
 - DhcpSetClientInfoVQ
 - dhcpsapi/DhcpSetClientInfoVQ
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
 - DhcpSetClientInfoVQ
---

# DhcpSetClientInfoVQ function


## -description

The <b>DhcpSetClientInfoVQ</b> function sets or modifies an existing DHCP client lease record in the DHCP server record database.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a> structure that contains the DHCP client lease record to add to or modify in the DHCP server database.

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
An error occurred while accessing the DHCPv6 server's database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The provided client hardware address data is <b>NULL</b> or the length is set to zero, or the subnet mask is incorrect.

</td>
</tr>
</table>