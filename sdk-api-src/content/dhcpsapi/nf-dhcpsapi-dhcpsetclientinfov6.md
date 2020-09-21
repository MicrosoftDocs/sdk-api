---
UID: NF:dhcpsapi.DhcpSetClientInfoV6
title: DhcpSetClientInfoV6 function (dhcpsapi.h)
description: Sets or modifies the reserved DHCPv6 client lease record in the DHCPv6 server database.
helpviewer_keywords: ["DhcpSetClientInfoV6","DhcpSetClientInfoV6 function [DHCP]","dhcp.dhcpsetclientinfov6","dhcpsapi/DhcpSetClientInfoV6"]
old-location: dhcp\dhcpsetclientinfov6.htm
tech.root: DHCP
ms.assetid: 35d976a9-4b5a-4a1f-b7d9-2f7b396baf01
ms.date: 12/05/2018
ms.keywords: DhcpSetClientInfoV6, DhcpSetClientInfoV6 function [DHCP], dhcp.dhcpsetclientinfov6, dhcpsapi/DhcpSetClientInfoV6
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
 - DhcpSetClientInfoV6
 - dhcpsapi/DhcpSetClientInfoV6
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
 - DhcpSetClientInfoV6
---

# DhcpSetClientInfoV6 function


## -description

The <b>DhcpSetClientInfoV6</b> function sets or modifies the reserved DHCPv6 client lease record in the DHCPv6 server database.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v6">DHCP_CLIENT_INFO_V6</a> structure that contains the updated DHCPv6 client leaser record information.

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
</table>

## -remarks

<div class="alert"><b>Note</b>  This method must be called only after the DHCPv6 client has been added by previously calling <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddsubnetelementv6">DhcpAddSubnetElementV6</a>.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddsubnetelementv6">DhcpAddSubnetElementV6</a>