---
UID: NF:dhcpsapi.DhcpCreateClientInfoV4
title: DhcpCreateClientInfoV4 function (dhcpsapi.h)
description: Creates a client information record on the DHCP server, extending the functionality of DhcpCreateClientInfo by including the client type (DHCP or BOOTP) in the record.
helpviewer_keywords: ["DhcpCreateClientInfoV4","DhcpCreateClientInfoV4 function [DHCP]","dhcp.dhcpcreateclientinfov4","dhcpsapi/DhcpCreateClientInfoV4"]
old-location: dhcp\dhcpcreateclientinfov4.htm
tech.root: DHCP
ms.assetid: 0657e107-bf3d-4bcd-88a1-84a6cd7f934d
ms.date: 12/05/2018
ms.keywords: DhcpCreateClientInfoV4, DhcpCreateClientInfoV4 function [DHCP], dhcp.dhcpcreateclientinfov4, dhcpsapi/DhcpCreateClientInfoV4
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
 - DhcpCreateClientInfoV4
 - dhcpsapi/DhcpCreateClientInfoV4
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
 - DhcpCreateClientInfoV4
---

# DhcpCreateClientInfoV4 function


## -description

The <b>DhcpCreateClientInfoV4</b> function creates a client information record on the DHCP server, extending the functionality of <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateclientinfo">DhcpCreateClientInfo</a> by including the client type (DHCP or BOOTP) in the record.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a> structure that contains information about the DHCP client, including the assigned IP address, the subnet mask, the  host, and the client type (DHCP and/or BOOTP).

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
</table>

## -remarks

When successful, a call to this additionally marks the specified DHCP client IPv4 address as unavailable, in order to avoid IP duplication.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_v4">DHCP_CLIENT_INFO_V4</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpcreateclientinfo">DhcpCreateClientInfo</a>