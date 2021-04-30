---
UID: NF:dhcpsapi.DhcpGetClientOptions
title: DhcpGetClientOptions function (dhcpsapi.h)
description: Returns only ERROR_NOT_IMPLEMENTED, as it is not used or supported.
helpviewer_keywords: ["DhcpGetClientOptions","DhcpGetClientOptions function [DHCP]","dhcp.dhcpgetclientoptions","dhcpsapi/DhcpGetClientOptions"]
old-location: dhcp\dhcpgetclientoptions.htm
tech.root: DHCP
ms.assetid: 60f4db5f-0359-4738-980e-2a56adbf551e
ms.date: 12/05/2018
ms.keywords: DhcpGetClientOptions, DhcpGetClientOptions function [DHCP], dhcp.dhcpgetclientoptions, dhcpsapi/DhcpGetClientOptions
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
 - DhcpGetClientOptions
 - dhcpsapi/DhcpGetClientOptions
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
 - DhcpGetClientOptions
---

# DhcpGetClientOptions function


## -description

The <b>DhcpGetClientOptions</b> function returns only ERROR_NOT_IMPLEMENTED, as it is not used or supported.

## -parameters

### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ClientIpAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> value that specifies the IP address or hostname of the DHCP client  whose option values will be returned.

### -param ClientSubnetMask [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_MASK</a> value that specifies the subnet mask of the DHCP client whose option values will be returned.

### -param ClientOptions [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_list">DHCP_OPTION_LIST</a> structure that contains the returned option values for the DHCP client.

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
<dt><b>ERROR_NOT_IMPLEMENTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not implemented and is not supported.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_option_list">DHCP_OPTION_LIST</a>