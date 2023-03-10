---
UID: NF:dhcpsapi.DhcpGetClientInfoVQ
title: DhcpGetClientInfoVQ function (dhcpsapi.h)
description: Retrieves DHCP client lease record information from the DHCP server database. (DhcpGetClientInfoVQ)
helpviewer_keywords: ["DhcpGetClientInfoVQ","DhcpGetClientInfoVQ function [DHCP]","dhcp.dhcpgetclientinfovq","dhcpsapi/DhcpGetClientInfoVQ"]
old-location: dhcp\dhcpgetclientinfovq.htm
tech.root: DHCP
ms.assetid: e8ed729b-12c2-4179-b7ef-6c71acf2672e
ms.date: 12/05/2018
ms.keywords: DhcpGetClientInfoVQ, DhcpGetClientInfoVQ function [DHCP], dhcp.dhcpgetclientinfovq, dhcpsapi/DhcpGetClientInfoVQ
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
 - DhcpGetClientInfoVQ
 - dhcpsapi/DhcpGetClientInfoVQ
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
 - DhcpGetClientInfoVQ
---

# DhcpGetClientInfoVQ function


## -description

The <b>DhcpGetClientInfoVQ</b> function retrieves DHCP client lease record information from the DHCP server database.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param SearchInfo [in]

Pointer to a <a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a> structure that defines the key used to search the client lease record database on the DHCP server for a particular client record.

### -param ClientInfo [out]

Pointer to the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a> structure returned by a successful search operation.

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

## -remarks

The caller of this function must release the memory used by the <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a> structure returned in <i>ClientInfo</i>.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_client_info_vq">DHCP_CLIENT_INFO_VQ</a>



<a href="/windows/win32/api/dhcpsapi/ns-dhcpsapi-dhcp_search_info">DHCP_SEARCH_INFO</a>
