---
UID: NF:dhcpsapi.DhcpV6CreateClientInfo
title: DhcpV6CreateClientInfo function (dhcpsapi.h)
description: Creates a DHCPv6 client lease record in the DHCP server database.
helpviewer_keywords: ["DhcpV6CreateClientInfo","DhcpV6CreateClientInfo function [DHCP]","dhcp.dhcpv6createclientinfo","dhcpsapi/DhcpV6CreateClientInfo"]
old-location: dhcp\dhcpv6createclientinfo.htm
tech.root: DHCP
ms.assetid: 5d49ab90-3c40-4577-8e7e-36d1370d8de9
ms.date: 12/05/2018
ms.keywords: DhcpV6CreateClientInfo, DhcpV6CreateClientInfo function [DHCP], dhcp.dhcpv6createclientinfo, dhcpsapi/DhcpV6CreateClientInfo
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
 - DhcpV6CreateClientInfo
 - dhcpsapi/DhcpV6CreateClientInfo
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
 - DhcpV6CreateClientInfo
---

# DhcpV6CreateClientInfo function


## -description

The <b>DhcpV6CreateClientInfo</b> function  creates a DHCPv6 client lease record in the DHCP server database.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v6">DHCP_CLIENT_INFO_V6</a> structure that contains the DHCP client lease record information. The <b>ClientIpAddress</b>, <b>ClientDUID</b> and <b>IAID</b> fields of this structure are required, all others are optional.

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
<b>ClientDUID</b> in the <i>ClientInfo</i> parameter was <b>NULL</b> or a zero length buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
This call was performed by a client that is not a member of the <i>DHCP Administrators</i> security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified subnet does not exist. In this case, there is no subnet corresponding to <b>ClientIpAddress</b> in the <i>ClientInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLIENT_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The provided DHCP client record already exists in the DHCP server database.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4createclientinfo">DhcpV4CreateClientInfo</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getclientinfo">DhcpV4GetClientInfo</a>