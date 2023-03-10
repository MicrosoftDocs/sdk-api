---
UID: NF:dhcpsapi.DhcpV4EnumPolicies
title: DhcpV4EnumPolicies function (dhcpsapi.h)
description: Enumerates the policies configured on the DHCP Server.
helpviewer_keywords: ["DhcpV4EnumPolicies","DhcpV4EnumPolicies function [DHCP]","dhcp.dhcpv4enumpolicies","dhcpsapi/DhcpV4EnumPolicies"]
old-location: dhcp\dhcpv4enumpolicies.htm
tech.root: DHCP
ms.assetid: c3915699-f60d-495c-81df-85dc6fe2657c
ms.date: 12/05/2018
ms.keywords: DhcpV4EnumPolicies, DhcpV4EnumPolicies function [DHCP], dhcp.dhcpv4enumpolicies, dhcpsapi/DhcpV4EnumPolicies
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
 - DhcpV4EnumPolicies
 - dhcpsapi/DhcpV4EnumPolicies
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
 - DhcpV4EnumPolicies
---

# DhcpV4EnumPolicies function


## -description

The <b>DhcpV4EnumPolicies</b> function enumerates the policies configured on the DHCP Server.

## -parameters

### -param ServerIpAddress [in, optional]

Pointer to a null-terminated Unicode string that represents the IP address or hostname of the DHCP server.

### -param ResumeHandle [in, out]

Pointer to a  <a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_RESUME_HANDLE</a> structure that identifies this enumeration for use in subsequent calls to this function.

Initially, this value should be zero on input. If successful, the returned value should be used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100, and 200 policies are configured on the server, the resume handle can be used after the first 100 policies are retrieved to obtain the next 100 on a subsequent call.

### -param PreferredMaximum [in]

The maximum number of policy structures to return in <i>EnumInfo</i>. If <i>PreferredMaximum</i> is greater than the number of remaining non-enumerated policies on the server, the remaining number of  non-enumerated policies is returned.

### -param fGlobalPolicy [in]

If <b>TRUE</b> the server level policy is enumerated. Otherwise, the scope level policy is enumerated.

### -param SubnetAddress [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the policies to enumerate.

### -param EnumInfo [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy_array">DHCP_POLICY_ARRAY</a> structure that contains the policies available on the DHCP server. If no policies are configured, this value is <b>NULL</b>.

### -param ElementsRead [out]

Pointer to a <b>DWORD</b> that specifies the number of policies returned in <i>EnumInfo</i>.

### -param ElementsTotal [out]

Pointer to a <b>DWORD</b>  that specifies the number of policies configured on the DHCP server that have not yet been enumerated.

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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are more elements available to enumerate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
There are no more elements left to enumerate.

</td>
</tr>
</table>

## -remarks

<i>EnumInfo</i> should be free using <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcprpcfreememory">DhcpRpcFreeMemory</a>.

<i>SubnetAddress</i> must be in host-byte ordering.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4addpolicyrange">DhcpV4AddPolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4createpolicy">DhcpV4CreatePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4deletepolicy">DhcpV4DeletePolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4getpolicy">DhcpV4GetPolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4querypolicyenforcement">DhcpV4QueryPolicyEnforcement</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4removepolicyrange">DhcpV4RemovePolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicy">DhcpV4SetPolicy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpv4setpolicyenforcement">DhcpV4SetPolicyEnforcement</a>