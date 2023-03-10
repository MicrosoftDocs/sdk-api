---
UID: NF:dhcpsapi.DhcpV4RemovePolicyRange
title: DhcpV4RemovePolicyRange function (dhcpsapi.h)
description: Removes the specified IP address range from the list of IP address ranges of the policy.
helpviewer_keywords: ["DhcpV4RemovePolicyRange","DhcpV4RemovePolicyRange function [DHCP]","dhcp.dhcpv4removepolicyrange","dhcpsapi/DhcpV4RemovePolicyRange"]
old-location: dhcp\dhcpv4removepolicyrange.htm
tech.root: DHCP
ms.assetid: 2799e869-e9dd-41de-b808-8e4c52ee9ecf
ms.date: 12/05/2018
ms.keywords: DhcpV4RemovePolicyRange, DhcpV4RemovePolicyRange function [DHCP], dhcp.dhcpv4removepolicyrange, dhcpsapi/DhcpV4RemovePolicyRange
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
 - DhcpV4RemovePolicyRange
 - dhcpsapi/DhcpV4RemovePolicyRange
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
 - DhcpV4RemovePolicyRange
---

# DhcpV4RemovePolicyRange function


## -description

The <b>DhcpV4RemovePolicyRange</b> function  removes the specified IP address range from the list of IP address ranges of the policy.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policy IP address range to remove.

### -param PolicyName [in]

A null-terminated Unicode string that represents the name of the policy IP address range to remove.

### -param Range [in]

A pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_ip_range">DHCP_IP_RANGE</a> structure that  contains the policy IP address range to remove.

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
The specified IPv4 subnet does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified policy does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_RANGE_BAD</b></dt>
</dl>
</td>
<td width="60%">
The specified policy range is not contained within the IP address range of the scope.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4addpolicyrange">DhcpV4AddPolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4createpolicy">DhcpV4CreatePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4deletepolicy">DhcpV4DeletePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4enumpolicies">DhcpV4EnumPolicies</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getpolicy">DhcpV4GetPolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4querypolicyenforcement">DhcpV4QueryPolicyEnforcement</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicy">DhcpV4SetPolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicyenforcement">DhcpV4SetPolicyEnforcement</a>