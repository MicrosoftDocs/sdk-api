---
UID: NF:dhcpsapi.DhcpGetClientInfoV6
title: DhcpGetClientInfoV6 function (dhcpsapi.h)
description: Retrieves IPv6 address lease information for a specific IPv6 client reservation from the DHCPv6 server.
helpviewer_keywords: ["DhcpGetClientInfoV6","DhcpGetClientInfoV6 function [DHCP]","dhcp.dhcpgetclientinfov6","dhcpsapi/DhcpGetClientInfoV6"]
old-location: dhcp\dhcpgetclientinfov6.htm
tech.root: DHCP
ms.assetid: 6ed68064-9f12-472e-8647-87cc50345199
ms.date: 12/05/2018
ms.keywords: DhcpGetClientInfoV6, DhcpGetClientInfoV6 function [DHCP], dhcp.dhcpgetclientinfov6, dhcpsapi/DhcpGetClientInfoV6
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
 - DhcpGetClientInfoV6
 - dhcpsapi/DhcpGetClientInfoV6
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
 - DhcpGetClientInfoV6
---

# DhcpGetClientInfoV6 function


## -description

The <b>DhcpGetClientInfoV6</b> function retrieves IPv6 address lease information for a specific IPv6 client reservation from the DHCPv6 server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SearchInfo [in]

Pointer to a <a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info_v6">DHCP_SEARCH_INFO_V6</a> structure that contains the search parameters for finding the specific IPv6 lease information for a client. The <b>SearchType</b> member of this structure must be set to <b>Dhcpv6ClientIpAddress</b>.

### -param ClientInfo [out]

Pointer to the address of a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v6">DHCP_CLIENT_INFO_V6</a> structure that contains the IPv6 address lease information that matched the parameters supplied in <i>SearchInfo</i>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Either <b>Dhcpc6ClientDuid</b> or <b>Dhcpv6ClientName</b> was specified for the <b>SearchType</b> member of <i>SearchInfo</i>.

</td>
</tr>
</table>