---
UID: NF:dhcpsapi.DhcpV6GetFreeIPAddress
title: DhcpV6GetFreeIPAddress function (dhcpsapi.h)
description: Retrieves the list of available IPv6 addresses that can be leased to clients.
helpviewer_keywords: ["DhcpV6GetFreeIPAddress","DhcpV6GetFreeIPAddress function [DHCP]","dhcp.dhcpv6getfreeipaddress","dhcpsapi/DhcpV6GetFreeIPAddress"]
old-location: dhcp\dhcpv6getfreeipaddress.htm
tech.root: DHCP
ms.assetid: 4448bbfb-5942-42f9-8daf-3bf86e124052
ms.date: 12/05/2018
ms.keywords: DhcpV6GetFreeIPAddress, DhcpV6GetFreeIPAddress function [DHCP], dhcp.dhcpv6getfreeipaddress, dhcpsapi/DhcpV6GetFreeIPAddress
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
 - DhcpV6GetFreeIPAddress
 - dhcpsapi/DhcpV6GetFreeIPAddress
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
 - DhcpV6GetFreeIPAddress
---

# DhcpV6GetFreeIPAddress function


## -description

The <b>DhcpV6GetFreeIPAddress</b> function  retrieves the list of available IPv6 addresses that can be leased to clients.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param ScopeId [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that specifies the IPv6 subnet ID from which available addresses to lease to clients are retrieved.

### -param StartIP [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that specifies the scope IPv6 range's starting point address from where the available addresses are retrieved. If this parameter is 0, the start address of the IPv6 subnet specified by <i>ScopeId</i> is the default.

### -param EndIP [in]

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that specifies the scope IPv6 range's end point address from where the available addresses are retrieved. If this parameter is 0, the end address of the IPv6 subnet specified by <i>ScopeId</i> parameter is taken as the default.

### -param NumFreeAddrReq [in]

Integer that specifies the number of IPv6 addresses retrieved from the specified scope in <i>IPAddrList</i>. If this parameter is 0, only one IPv6 address is returned.

### -param IPAddrList [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_ip_array">DHCPV6_IP_ARRAY</a> structure that contains the list of available IPv6 addresses that can be leased to clients.

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
One or more of the parameters were invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_SUBNET_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
IPv6 subnet does not exist on the DHCP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_REACHED_END_OF_SELECTION</b></dt>
</dl>
</td>
<td width="60%">
The specified DHCP server has reached the end of the selected range while finding the free IP address.

</td>
</tr>
</table>

## -remarks

<i>IPAddrList</i> should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

The maximum number of IPv6 addresses returned is 1024. To retrieve more that 1024 IPv6 addresses, multiple calls to  <b>DhcpV6GetFreeIPAddress</b> must be made. After the initial call, each subsequent call to <b>DhcpV6GetFreeIPAddress</b> must set <i>startIP</i> to the last address in the list received in <i>IPAddrList</i> from the previous call to <b>DhcpV6GetFreeIPAddress</b>.

When the number of free IPv6 addresses available on the DHCP server is less than that requested, the list of free IPv6 addresses available are returned to the caller with error code <b>ERROR_DHCP_REACHED_END_OF_SELECTION</b>.