---
UID: NF:dhcpsapi.DhcpV4SetPolicyEnforcement
title: DhcpV4SetPolicyEnforcement function (dhcpsapi.h)
description: Sets the policy enforcement state of the server or the specified IPv4 subnet on the DHCP Server.
helpviewer_keywords: ["DhcpV4SetPolicyEnforcement","DhcpV4SetPolicyEnforcement function [DHCP]","dhcp.dhcpv4setpolicyenforcement","dhcpsapi/DhcpV4SetPolicyEnforcement"]
old-location: dhcp\dhcpv4setpolicyenforcement.htm
tech.root: DHCP
ms.assetid: 1e87942a-3ee1-442a-a56a-8e63b3003d3b
ms.date: 12/05/2018
ms.keywords: DhcpV4SetPolicyEnforcement, DhcpV4SetPolicyEnforcement function [DHCP], dhcp.dhcpv4setpolicyenforcement, dhcpsapi/DhcpV4SetPolicyEnforcement
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
 - DhcpV4SetPolicyEnforcement
 - dhcpsapi/DhcpV4SetPolicyEnforcement
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
 - DhcpV4SetPolicyEnforcement
---

# DhcpV4SetPolicyEnforcement function


## -description

The <b>DhcpV4SetPolicyEnforcement</b> function  sets the policy enforcement state of the server or the specified IPv4 subnet on the DHCP Server.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param fGlobalPolicy [in]

If <b>TRUE</b> the policy enforcement state of the server is set. Otherwise, the policy enforcement state of specified Ipv4 scope is set.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policy enforcement state to set.

### -param Enable [in]

If  <b>TRUE</b> the policy enforcement state is enabled. Otherwise, the policy enforcement state is disabled.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4addpolicyrange">DhcpV4AddPolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4createpolicy">DhcpV4CreatePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4deletepolicy">DhcpV4DeletePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4enumpolicies">DhcpV4EnumPolicies</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getpolicy">DhcpV4GetPolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4querypolicyenforcement">DhcpV4QueryPolicyEnforcement</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removepolicyrange">DhcpV4RemovePolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicy">DhcpV4SetPolicy</a>