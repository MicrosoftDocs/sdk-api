---
UID: NF:dhcpsapi.DhcpV4GetPolicy
title: DhcpV4GetPolicy function (dhcpsapi.h)
description: Retrieves a policy from the DHCP Server.
helpviewer_keywords: ["DhcpV4GetPolicy","DhcpV4GetPolicy function [DHCP]","dhcp.dhcpv4getpolicy","dhcpsapi/DhcpV4GetPolicy"]
old-location: dhcp\dhcpv4getpolicy.htm
tech.root: DHCP
ms.assetid: a6112bf8-5c1f-4f33-ba1f-b4903cc6befa
ms.date: 12/05/2018
ms.keywords: DhcpV4GetPolicy, DhcpV4GetPolicy function [DHCP], dhcp.dhcpv4getpolicy, dhcpsapi/DhcpV4GetPolicy
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
 - DhcpV4GetPolicy
 - dhcpsapi/DhcpV4GetPolicy
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
 - DhcpV4GetPolicy
---

# DhcpV4GetPolicy function


## -description

The <b>DhcpV4GetPolicy</b> function retrieves a policy from the DHCP Server.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param fGlobalPolicy [in]

If <b>TRUE</b> the server level policy is retrieved. Otherwise, the scope level policy is retrieved.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policy to retrieve.

### -param PolicyName [in]

A null-terminated Unicode string that represents the name of the policy to retrieve.

### -param Policy [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the parameters of the policy requested in <i>PolicyName</i>.

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
The DHCP server policy was not found.

</td>
</tr>
</table>

## -remarks

<i>Policy</i> should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4addpolicyrange">DhcpV4AddPolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4createpolicy">DhcpV4CreatePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4deletepolicy">DhcpV4DeletePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4enumpolicies">DhcpV4EnumPolicies</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4querypolicyenforcement">DhcpV4QueryPolicyEnforcement</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removepolicyrange">DhcpV4RemovePolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicy">DhcpV4SetPolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicyenforcement">DhcpV4SetPolicyEnforcement</a>