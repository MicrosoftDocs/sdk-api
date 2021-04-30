---
UID: NF:dhcpsapi.DhcpHlprAddV4PolicyExpr
title: DhcpHlprAddV4PolicyExpr function (dhcpsapi.h)
description: Allocates, initializes, and adds a DHCP server policy expression to a DHCP server policy.
helpviewer_keywords: ["DhcpHlprAddV4PolicyExpr","DhcpHlprAddV4PolicyExpr function [DHCP]","dhcp.dhcphlpraddv4policyexpr","dhcpsapi/DhcpHlprAddV4PolicyExpr"]
old-location: dhcp\dhcphlpraddv4policyexpr.htm
tech.root: DHCP
ms.assetid: 549d86ed-81c1-4126-9f43-f7e5340990d3
ms.date: 12/05/2018
ms.keywords: DhcpHlprAddV4PolicyExpr, DhcpHlprAddV4PolicyExpr function [DHCP], dhcp.dhcphlpraddv4policyexpr, dhcpsapi/DhcpHlprAddV4PolicyExpr
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
 - DhcpHlprAddV4PolicyExpr
 - dhcpsapi/DhcpHlprAddV4PolicyExpr
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
 - DhcpHlprAddV4PolicyExpr
---

# DhcpHlprAddV4PolicyExpr function


## -description

The <b>DhcpHlprAddV4PolicyExpr</b> function allocates, initializes, and adds a DHCP server policy expression to a DHCP server policy.

## -parameters

### -param Policy [in, out]

Pointer to a <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the policy to modify

### -param ParentExpr [in]

Integer that specifies the expression index that corresponds to this constituent condition.

### -param Operator [in]

A <a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_pol_logic_oper">DHCP_POL_LOGIC_OPER</a> enumeration that defines how the expression is to be evaluated in terms of the results of its constituents.

### -param ExprIndex [out]

Pointer to a <b>DWORD</b> that contains the newly created expression's index in the DHCP server policy.

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
One or more of the  parameters were invalid.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_POLICY_BAD_PARENT_EXPR</b></dt>
</dl>
</td>
<td width="60%">
The parent expression specified does not exist.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyrange">DhcpHlprAddV4PolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprcreatev4policy">DhcpHlprCreateV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprfreev4policy">DhcpHlprFreeV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policysingleuc">DhcpHlprIsV4PolicySingleUC</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policyvalid">DhcpHlprIsV4PolicyValid</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policywellformed">DhcpHlprIsV4PolicyWellFormed</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprmodifyv4policyexpr">DhcpHlprModifyV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprresetv4policyexpr">DhcpHlprResetV4PolicyExpr</a>