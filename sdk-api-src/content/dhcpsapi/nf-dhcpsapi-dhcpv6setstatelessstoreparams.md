---
UID: NF:dhcpsapi.DhcpV6SetStatelessStoreParams
title: DhcpV6SetStatelessStoreParams function (dhcpsapi.h)
description: Sets the DHCPv6 stateless client inventory configuration settings at the server or scope level.
helpviewer_keywords: ["DhcpV6SetStatelessStoreParams","DhcpV6SetStatelessStoreParams function [DHCP]","dhcp.dhcpv6setstatelessstoreparams","dhcpsapi/DhcpV6SetStatelessStoreParams"]
old-location: dhcp\dhcpv6setstatelessstoreparams.htm
tech.root: DHCP
ms.assetid: 8f64c1bb-8f02-45e3-b9ed-8fce2bf9885c
ms.date: 12/05/2018
ms.keywords: DhcpV6SetStatelessStoreParams, DhcpV6SetStatelessStoreParams function [DHCP], dhcp.dhcpv6setstatelessstoreparams, dhcpsapi/DhcpV6SetStatelessStoreParams
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
 - DhcpV6SetStatelessStoreParams
 - dhcpsapi/DhcpV6SetStatelessStoreParams
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
 - DhcpV6SetStatelessStoreParams
---

# DhcpV6SetStatelessStoreParams function


## -description

The <b>DhcpV6SetStatelessStoreParams</b> function  sets the DHCPv6 stateless client inventory configuration settings at the server or scope level.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.

### -param fServerLevel [in]

If <b>TRUE</b> the stateless client inventory configuration settings at server level are modified. Otherwise, the scope level configuration settings are modified.

### -param SubnetAddress [in]

A <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ipv6_address">DHCP_IPV6_ADDRESS</a> structure that contains the IPv6 subnet address of the stateless client inventory configuration settings to be modified. 
If the value of <i>fServerLevel</i> is <b>TRUE</b>, this must be 0.

### -param FieldModified [in]

A value from the <a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcpv6_stateless_param_type">DHCPV6_STATELESS_PARAM_TYPE</a> enumeration that defines the DHCPv6 stateless client inventory configuration parameter type to be modified.

### -param Params [in]

Pointer to a <a href="/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_stateless_params">DHCPV6_STATELESS_PARAMS</a> structure that contains the stateless client inventory configuration settings for a DHCPv6 server.

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
IPv6 subnet does not exist on the DHCPv6 server.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv6getstatelessstatistics">DhcpV6GetStatelessStatistics</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv6getstatelessstoreparams">DhcpV6GetStatelessStoreParams</a>