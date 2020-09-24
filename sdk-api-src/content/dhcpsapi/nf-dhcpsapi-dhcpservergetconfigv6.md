---
UID: NF:dhcpsapi.DhcpServerGetConfigV6
title: DhcpServerGetConfigV6 function (dhcpsapi.h)
description: Retrieves the configuration information for the DHCPv6 server.
helpviewer_keywords: ["DhcpServerGetConfigV6","DhcpServerGetConfigV6 function [DHCP]","dhcp.dhcpservergetconfigv6","dhcpsapi/DhcpServerGetConfigV6"]
old-location: dhcp\dhcpservergetconfigv6.htm
tech.root: DHCP
ms.assetid: a867d8fe-0222-44aa-a00a-65a94cf59730
ms.date: 12/05/2018
ms.keywords: DhcpServerGetConfigV6, DhcpServerGetConfigV6 function [DHCP], dhcp.dhcpservergetconfigv6, dhcpsapi/DhcpServerGetConfigV6
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
 - DhcpServerGetConfigV6
 - dhcpsapi/DhcpServerGetConfigV6
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
 - DhcpServerGetConfigV6
---

# DhcpServerGetConfigV6 function


## -description

The <b>DhcpServerGetConfigV6</b> function retrieves the configuration information for the DHCPv6 server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ScopeInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info6">DHCP_OPTION_SCOPE_INFO6</a> structure used to identify the DHCPv6 scope for which configuration information will be retrieved.

### -param ConfigInfo [out]

Pointer to the address of a  <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v6">DHCP_SERVER_CONFIG_INFO_V6</a> structure that contains the requested configuration information.

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

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_scope_info6">DHCP_OPTION_SCOPE_INFO6</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_server_config_info_v6">DHCP_SERVER_CONFIG_INFO_V6</a>