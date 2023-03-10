---
UID: NF:dhcpsapi.DhcpGetFilterV4
title: DhcpGetFilterV4 function (dhcpsapi.h)
description: Retrieves the enable/disable settings for the DHCPv4 server's allow/deny lists.
helpviewer_keywords: ["DhcpGetFilterV4","DhcpGetFilterV4 function [DHCP]","dhcp.dhcpgetfilterv4","dhcpsapi/DhcpGetFilterV4"]
old-location: dhcp\dhcpgetfilterv4.htm
tech.root: DHCP
ms.assetid: 2acee985-48b1-4a76-9ca1-2fc27d990032
ms.date: 12/05/2018
ms.keywords: DhcpGetFilterV4, DhcpGetFilterV4 function [DHCP], dhcp.dhcpgetfilterv4, dhcpsapi/DhcpGetFilterV4
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
 - DhcpGetFilterV4
 - dhcpsapi/DhcpGetFilterV4
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
 - DhcpGetFilterV4
---

# DhcpGetFilterV4 function


## -description

The <b>DhcpGetFilterV4</b> function retrieves the enable/disable settings for the DHCPv4 server's allow/deny lists.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param GlobalFilterInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_filter_global_info">DHCP_FILTER_GLOBAL_INFO</a> structure that contains the enable/disable settings for the DHCPv6 server's allow/deny lists.

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

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_filter_global_info">DHCP_FILTER_GLOBAL_INFO</a>