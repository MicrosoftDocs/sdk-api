---
UID: NF:dhcpsapi.DhcpEnumSubnetsV6
title: DhcpEnumSubnetsV6 function (dhcpsapi.h)
description: The DhcpEnumSubnetsV6 function returns an enumerated list of subnets defined on the DHCP server.
helpviewer_keywords: ["DhcpEnumSubnetsV6","DhcpEnumSubnetsV6 function [DHCP]","dhcp.dhcpenumsubnetsv6","dhcpsapi/DhcpEnumSubnetsV6"]
old-location: dhcp\dhcpenumsubnetsv6.htm
tech.root: DHCP
ms.assetid: 8e706ae7-6c4d-423d-a652-a101384104e8
ms.date: 12/05/2018
ms.keywords: DhcpEnumSubnetsV6, DhcpEnumSubnetsV6 function [DHCP], dhcp.dhcpenumsubnetsv6, dhcpsapi/DhcpEnumSubnetsV6
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - DhcpEnumSubnetsV6
 - dhcpsapi/DhcpEnumSubnetsV6
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
 - DhcpEnumSubnetsV6
---

# DhcpEnumSubnetsV6 function


## -description

The <b>DhcpEnumSubnetsV6</b> function returns an enumerated list of subnets defined on the DHCP server.

## -parameters

### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param ResumeHandle [in, out]

Pointer to a <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100, and 200 subnet addresses  are stored on the server, the resume handle can be used after the first 100 subnets are retrieved to obtain the next 100 on a subsequent call, and so forth.

### -param PreferredMaximum [in]

Specifies the preferred maximum number of subnet addresses to return. If the number of remaining unenumerated options is less than this value, then that amount will be returned.

### -param EnumInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_ip_array">DHCPV6_IP_ARRAY</a> structure that contains the subnet IDs available on the DHCP server. If no subnets are defined, this value will be null.

### -param ElementsRead [out]

Pointer to a <b>DWORD</b> value that specifies the number of subnet addresses returned in <i>EnumInfo</i>.

### -param ElementsTotal [out]

Pointer to a <b>DWORD</b> value that specifies the  number of subnets defined on the DHCP server that have not yet been enumerated.

## -returns

This function returns <b>ERROR_SUCCESS</b> upon a successful call. If a call is made with the same <i>ResumeHandle</i> value and all items on the server have been enumerated, this method returns <b>ERROR_NO_MORE_ITEMS</b> with <i>ElementsRead</i> and <i>ElementsTotal</i> set to 0. Otherwise, it returns one of the <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-api-error-codes">DHCP Server Management API Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more items to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More data is available to enumerate.

</td>
</tr>
</table>