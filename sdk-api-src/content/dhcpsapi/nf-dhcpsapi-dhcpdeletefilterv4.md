---
UID: NF:dhcpsapi.DhcpDeleteFilterV4
title: DhcpDeleteFilterV4 function (dhcpsapi.h)
description: Deletes a link-layer address or address pattern from a DHCP server's allow/deny lists.
helpviewer_keywords: ["DhcpDeleteFilterV4","DhcpDeleteFilterV4 function [DHCP]","dhcp.dhcpdeletefilterv4","dhcpsapi/DhcpDeleteFilterV4"]
old-location: dhcp\dhcpdeletefilterv4.htm
tech.root: DHCP
ms.assetid: ba59bfed-63dd-4468-bc2a-ed47d093c23c
ms.date: 12/05/2018
ms.keywords: DhcpDeleteFilterV4, DhcpDeleteFilterV4 function [DHCP], dhcp.dhcpdeletefilterv4, dhcpsapi/DhcpDeleteFilterV4
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
 - DhcpDeleteFilterV4
 - dhcpsapi/DhcpDeleteFilterV4
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
 - DhcpDeleteFilterV4
---

# DhcpDeleteFilterV4 function


## -description

The <b>DhcpDeleteFilterV4</b> function deletes a link-layer address or address pattern from a DHCP server's allow/deny lists.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param DeleteFilterInfo [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_addr_pattern">DHCP_ADDR_PATTERN</a> structure that contains the link-layer address or address pattern filter to remove from the DHCP server database.

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
<dt><b>ERROR_DHCP_LINKLAYER_ADDRESS_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The address or address pattern does not exist in an allow/deny list.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The address or address pattern supplied in <i>DeleteFilterInfo</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_addr_pattern">DHCP_ADDR_PATTERN</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpaddfilterv4">DhcpAddFilterV4</a>