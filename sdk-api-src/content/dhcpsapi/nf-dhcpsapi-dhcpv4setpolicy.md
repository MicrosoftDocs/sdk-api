---
UID: NF:dhcpsapi.DhcpV4SetPolicy
title: DhcpV4SetPolicy function (dhcpsapi.h)
description: Updates one or more parameters of an existing policy.
helpviewer_keywords: ["DhcpV4SetPolicy","DhcpV4SetPolicy function [DHCP]","dhcp.dhcpv4setpolicy","dhcpsapi/DhcpV4SetPolicy"]
old-location: dhcp\dhcpv4setpolicy.htm
tech.root: DHCP
ms.assetid: 1e51aea4-f56f-4a7c-95eb-e955e7d173ca
ms.date: 12/05/2018
ms.keywords: DhcpV4SetPolicy, DhcpV4SetPolicy function [DHCP], dhcp.dhcpv4setpolicy, dhcpsapi/DhcpV4SetPolicy
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
 - DhcpV4SetPolicy
 - dhcpsapi/DhcpV4SetPolicy
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
 - DhcpV4SetPolicy
---

# DhcpV4SetPolicy function


## -description

The <b>DhcpV4SetPolicy</b> function  updates one or more parameters of an existing policy.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param FieldsModified [in]

A value from the <a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_policy_fields_to_update">DHCP_POLICY_FIELDS_TO_UPDATE</a> enumeration that defines the DHCPv4 policy fields to modify.

### -param fGlobalPolicy [in]

If <b>TRUE</b> the server level policy is set. Otherwise, the scope level policy is set.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policy to modify.

### -param PolicyName [in]

A null-terminated Unicode string that represents the name of the policy to modify.

### -param Policy [in]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the parameters of the policy to modify.

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
<dt><b>ERROR_DHCP_RANGE_INVALID_IN_SERVER_POLICY</b></dt>
</dl>
</td>
<td width="60%">
A policy range has been specified for a server level policy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_POLICY_EXPRESSION</b></dt>
</dl>
</td>
<td width="60%">
The specified conditions or expressions of the policy are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_RANGE_BAD</b></dt>
</dl>
</td>
<td width="60%">
The specified policy range is not contained within the IP address range of the scope or the specified policy range is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_RANGE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The specified policy range overlaps with the policy ranges of an existing policy at the specified scope.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_INVALID_PROCESSING_ORDER</b></dt>
</dl>
</td>
<td width="60%">
The specified processing order is greater than the maximum processing order of the existing policies at the specified level (server or scope).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The vendor class or user class reference in the conditions of the policy does not exist.

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



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removepolicyrange">DhcpV4RemovePolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicyenforcement">DhcpV4SetPolicyEnforcement</a>