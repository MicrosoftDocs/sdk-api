---
UID: NF:dhcpsapi.DhcpHlprIsV4PolicyValid
title: DhcpHlprIsV4PolicyValid function (dhcpsapi.h)
description: Verifies a DHCP server policy.
helpviewer_keywords: ["DhcpHlprIsV4PolicyValid","DhcpHlprIsV4PolicyValid function [DHCP]","dhcp.dhcphlprisv4policyvalid","dhcpsapi/DhcpHlprIsV4PolicyValid"]
old-location: dhcp\dhcphlprisv4policyvalid.htm
tech.root: DHCP
ms.assetid: f11386a6-2b80-4a2b-b859-fb399d7392e8
ms.date: 12/05/2018
ms.keywords: DhcpHlprIsV4PolicyValid, DhcpHlprIsV4PolicyValid function [DHCP], dhcp.dhcphlprisv4policyvalid, dhcpsapi/DhcpHlprIsV4PolicyValid
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
 - DhcpHlprIsV4PolicyValid
 - dhcpsapi/DhcpHlprIsV4PolicyValid
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
 - DhcpHlprIsV4PolicyValid
---

# DhcpHlprIsV4PolicyValid function


## -description

The <b>DhcpHlprIsV4PolicyValid</b> function verifies a DHCP server policy.

## -parameters

### -param pPolicy [in]

Pointer to <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the policy to verify.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter was invalid.

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
<dt><b>ERROR_DHCP_POLICY_RANGE_BAD</b></dt>
</dl>
</td>
<td width="60%">
The specified policy range is not contained within the IP address range of the scope or the specified policy range is invalid.

</td>
</tr>
</table>

## -remarks

The API performs the following validations on the policy structure.
   

<ol>
<li>The policy must be well formed.</li>
<li>Server policies must not have any ranges.</li>
<li>Server policies must have the subnet address set to 0.0.0.0.</li>
<li>Scope policies must have a subnet address.</li>
<li>All associated ranges must be valid and non-overlapping.</li>
<li>For all expressions, the parent expression index must be set to 0.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyexpr">DhcpHlprAddV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyrange">DhcpHlprAddV4PolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprcreatev4policy">DhcpHlprCreateV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprfreev4policy">DhcpHlprFreeV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policysingleuc">DhcpHlprIsV4PolicySingleUC</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policywellformed">DhcpHlprIsV4PolicyWellFormed</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprmodifyv4policyexpr">DhcpHlprModifyV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprresetv4policyexpr">DhcpHlprResetV4PolicyExpr</a>