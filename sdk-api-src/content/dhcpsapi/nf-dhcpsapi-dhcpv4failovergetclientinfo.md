---
UID: NF:dhcpsapi.DhcpV4FailoverGetClientInfo
title: DhcpV4FailoverGetClientInfo function (dhcpsapi.h)
description: Retrieves the DHCPv4 client lease information.
helpviewer_keywords: ["DhcpV4FailoverGetClientInfo","DhcpV4FailoverGetClientInfo function [DHCP]","dhcp.dhcpv4failovergetclientinfo","dhcpsapi/DhcpV4FailoverGetClientInfo"]
old-location: dhcp\dhcpv4failovergetclientinfo.htm
tech.root: DHCP
ms.assetid: 125665d1-5af6-4d8f-b7fe-cdbff6a7b415
ms.date: 12/05/2018
ms.keywords: DhcpV4FailoverGetClientInfo, DhcpV4FailoverGetClientInfo function [DHCP], dhcp.dhcpv4failovergetclientinfo, dhcpsapi/DhcpV4FailoverGetClientInfo
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpV4FailoverGetClientInfo
 - dhcpsapi/DhcpV4FailoverGetClientInfo
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
 - DhcpV4FailoverGetClientInfo
---

# DhcpV4FailoverGetClientInfo function


## -description

The <b>DhcpV4FailoverGetClientInfo</b> function retrieves the DHCPv4 client lease information.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param SearchInfo [in]

Pointer to a <a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a> structure that defines the key used to search the DHCPv4 client lease record on the server. 
If the <b>SearchType</b> member of <i>SearchInfo</i> is <b>DhcpClientName</b> and there are multiple lease records with the same client name, the server will return client information for the client with the lowest numerical IP address.

### -param ClientInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv4_failover_client_info">DHCPV4_FAILOVER_CLIENT_INFO</a> structure that contains the retrieved DHCPv4 client lease record.

<div class="alert"><b>Note</b>  <p class="note">The memory for this parameter must be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

</div>
<div> </div>

## -returns

If the function succeeds, it returns <b>ERROR_SUCCESS</b>.

If the function fails, it returns one of the following or an error code from <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server database or the client entry is not present in the database.

</td>
</tr>
</table>