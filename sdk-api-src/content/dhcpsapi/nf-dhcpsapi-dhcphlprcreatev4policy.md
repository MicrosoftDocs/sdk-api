---
UID: NF:dhcpsapi.DhcpHlprCreateV4Policy
title: DhcpHlprCreateV4Policy function (dhcpsapi.h)
description: Allocates and initializes a DHCP server policy structure.
helpviewer_keywords: ["DhcpHlprCreateV4Policy","DhcpHlprCreateV4Policy function [DHCP]","dhcp.dhcphlprcreatev4policy","dhcpsapi/DhcpHlprCreateV4Policy"]
old-location: dhcp\dhcphlprcreatev4policy.htm
tech.root: DHCP
ms.assetid: 91f04578-9f15-44b4-8cf6-99be13d0395e
ms.date: 12/05/2018
ms.keywords: DhcpHlprCreateV4Policy, DhcpHlprCreateV4Policy function [DHCP], dhcp.dhcphlprcreatev4policy, dhcpsapi/DhcpHlprCreateV4Policy
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
 - DhcpHlprCreateV4Policy
 - dhcpsapi/DhcpHlprCreateV4Policy
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
 - DhcpHlprCreateV4Policy
---

# DhcpHlprCreateV4Policy function


## -description

The <b>DhcpHlprCreateV4Policy</b> function allocates and initializes a DHCP server policy structure.

## -parameters

### -param PolicyName [in]

A null-terminated unicode string that contains the name of the DHCP server policy to create.

### -param fGlobalPolicy [in]

If <b>TRUE</b> a server level policy is created. Otherwise, a scope level policy is created

### -param Subnet [in]

<a href="/previous-versions/windows/desktop/dhcp/dhcp-server-management-type-definitions">DHCP_IP_ADDRESS</a> structure that contains the IPv4 subnet address of the scope level policy to create.

### -param ProcessingOrder [in]

Integer that specifies the processing order of the DHCP server policy. 1 indicates the highest priority and <b>MAX_DWORD</b> indicates the lowest.

### -param RootOperator [in]

<a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_pol_logic_oper">DHCP_POL_LOGIC_OPER</a> enumeration that defines how the policy condition is to be evaluated in terms of the results of its constituents.

### -param Description [in]

A pointer to a null-terminated Unicode string that contains the description of the DHCP server policy.

### -param Enabled [in]

<b>TRUE</b> if the policy is enabled. Otherwise, it is <b>FALSE</b>.

### -param Policy [out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the parameters of the policy to create.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory available.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyexpr">DhcpHlprAddV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyrange">DhcpHlprAddV4PolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprfreev4policy">DhcpHlprFreeV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policysingleuc">DhcpHlprIsV4PolicySingleUC</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policyvalid">DhcpHlprIsV4PolicyValid</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policywellformed">DhcpHlprIsV4PolicyWellFormed</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprmodifyv4policyexpr">DhcpHlprModifyV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprresetv4policyexpr">DhcpHlprResetV4PolicyExpr</a>