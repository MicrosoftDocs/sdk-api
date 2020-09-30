---
UID: NF:dhcpsapi.DhcpGetClientInfoV4
title: DhcpGetClientInfoV4 function (dhcpsapi.h)
description: Returns information on a specific DHCP client. This function extends DhcpGetClientInfo by returning a DHCP_CLIENT_INFO_V4 structure that contains client type information.
helpviewer_keywords: ["DhcpGetClientInfoV4","DhcpGetClientInfoV4 function [DHCP]","dhcp.dhcpgetclientinfov4","dhcpsapi/DhcpGetClientInfoV4"]
old-location: dhcp\dhcpgetclientinfov4.htm
tech.root: DHCP
ms.assetid: 3f8b9cbb-f903-4a97-8a38-caf2210b6d48
ms.date: 12/05/2018
ms.keywords: DhcpGetClientInfoV4, DhcpGetClientInfoV4 function [DHCP], dhcp.dhcpgetclientinfov4, dhcpsapi/DhcpGetClientInfoV4
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
 - DhcpGetClientInfoV4
 - dhcpsapi/DhcpGetClientInfoV4
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
 - DhcpGetClientInfoV4
---

# DhcpGetClientInfoV4 function


## -description

The <b>DhcpGetClientInfoV4</b> function returns information on a specific DHCP client. This function extends <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclientinfo">DhcpGetClientInfo</a> by returning a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a> structure that contains client type information.

## -parameters

### -param ServerIpAddress [in]

Specifies the IP address of the DHCP server.

### -param SearchInfo [in]

<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a> structure that contains the search parameters used to select a specific DHCP client.

### -param ClientInfo [out]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a> structure that contains information that describes the DHCP client that most closely matches the provided search parameters. If no client could be found, this parameter will be null.

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
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a>



<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclientinfo">DhcpGetClientInfo</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetclientinfo">DhcpSetClientInfo</a>