---
UID: NF:dhcpsapi.DhcpAddFilterV4
title: DhcpAddFilterV4 function (dhcpsapi.h)
description: Adds a link-layer address or address pattern to the allow/deny lists.
helpviewer_keywords: ["DhcpAddFilterV4","DhcpAddFilterV4 function [DHCP]","dhcp.dhcpaddfilterv4","dhcpsapi/DhcpAddFilterV4"]
old-location: dhcp\dhcpaddfilterv4.htm
tech.root: DHCP
ms.assetid: 5543ef67-d095-44b8-b511-e6754aeb9881
ms.date: 12/05/2018
ms.keywords: DhcpAddFilterV4, DhcpAddFilterV4 function [DHCP], dhcp.dhcpaddfilterv4, dhcpsapi/DhcpAddFilterV4
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
 - DhcpAddFilterV4
 - dhcpsapi/DhcpAddFilterV4
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
 - DhcpAddFilterV4
---

# DhcpAddFilterV4 function


## -description

The <b>DhcpAddFilterV4</b> function adds a link-layer address or address pattern to the allow/deny lists.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param AddFilterInfo [in]

Pointer to a <a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_filter_add_info">DHCP_FILTER_ADD_INFO</a> structure that contains a link-layer address or address pattern to add to the DHCP server's allow/deny list.

### -param ForceFlag [in]

If <b>TRUE</b>, any existing matching filter is overwritten; if <b>FALSE</b>, the call fails with <b>ERROR_DHCP_LINKLAYER_ADDRESS_EXISTS</b>.

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
<dt><b>ERROR_DHCP_LINKLAYER_ADDRESS_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The address or address pattern already exists in an allow/deny list.

</td>
</tr>
</table>

## -remarks

This API allows DHCP clients whose addresses have been added to the allow list to obtain leases, and blocks those added to the deny list. The respective lists must be enabled with a call to <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetfilterv4">DhcpSetFilterV4</a>.

## -see-also

<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_filter_add_info">DHCP_FILTER_ADD_INFO</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetfilterv4">DhcpSetFilterV4</a>