---
UID: NF:dhcpsapi.DhcpSetClientInfoV4
title: DhcpSetClientInfoV4 function (dhcpsapi.h)
description: Sets information on a client whose IP address lease is administrated by the DHCP server. This function extends the functionality provided by DhcpSetClientInfo by allowing the caller to specify the client type (DHCP or BOOTP).
helpviewer_keywords: ["DhcpSetClientInfoV4","DhcpSetClientInfoV4 function [DHCP]","dhcp.dhcpsetclientinfov4","dhcpsapi/DhcpSetClientInfoV4"]
old-location: dhcp\dhcpsetclientinfov4.htm
tech.root: DHCP
ms.assetid: f7e1aa86-634e-48a7-ae2a-9c23277ed946
ms.date: 12/05/2018
ms.keywords: DhcpSetClientInfoV4, DhcpSetClientInfoV4 function [DHCP], dhcp.dhcpsetclientinfov4, dhcpsapi/DhcpSetClientInfoV4
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
 - DhcpSetClientInfoV4
 - dhcpsapi/DhcpSetClientInfoV4
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
 - DhcpSetClientInfoV4
---

# DhcpSetClientInfoV4 function


## -description

The <b>DhcpSetClientInfoV4</b> function sets information on a client whose IP address lease is administrated by the DHCP server. This function extends the functionality provided by <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetclientinfo">DhcpSetClientInfo</a> by allowing the caller to specify the client type (DHCP or BOOTP).

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a> structure that contains the information, including client type, for a client in a subnet served by the DHCP server.

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



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetclientinfo">DhcpGetClientInfoV4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetclientinfo">DhcpSetClientInfo</a>