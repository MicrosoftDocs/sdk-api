---
UID: NF:dhcpsapi.DhcpHlprModifyV4PolicyExpr
title: DhcpHlprModifyV4PolicyExpr function (dhcpsapi.h)
description: Modifies the DHCP server policy expression in a DHCP server policy structure.
helpviewer_keywords: ["DhcpHlprModifyV4PolicyExpr","DhcpHlprModifyV4PolicyExpr function [DHCP]","dhcp.dhcphlprmodifyv4policyexpr","dhcpsapi/DhcpHlprModifyV4PolicyExpr"]
old-location: dhcp\dhcphlprmodifyv4policyexpr.htm
tech.root: DHCP
ms.assetid: 5d6818f9-4e44-4f24-a489-84defd1117c0
ms.date: 12/05/2018
ms.keywords: DhcpHlprModifyV4PolicyExpr, DhcpHlprModifyV4PolicyExpr function [DHCP], dhcp.dhcphlprmodifyv4policyexpr, dhcpsapi/DhcpHlprModifyV4PolicyExpr
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
 - DhcpHlprModifyV4PolicyExpr
 - dhcpsapi/DhcpHlprModifyV4PolicyExpr
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
 - DhcpHlprModifyV4PolicyExpr
---

# DhcpHlprModifyV4PolicyExpr function


## -description

The <b>DhcpHlprModifyV4PolicyExpr</b> function modifies the DHCP server policy expression in a DHCP server policy structure.

## -parameters

### -param Policy [in, out]

Pointer to <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the policy to modify.

### -param Operator [in]

A <a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_pol_logic_oper">DHCP_POL_LOGIC_OPER</a> enumeration that defines how the policy condition is to be evaluated in terms of the results of its constituents.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyexpr">DhcpHlprAddV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyrange">DhcpHlprAddV4PolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprcreatev4policy">DhcpHlprCreateV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprfreev4policy">DhcpHlprFreeV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policysingleuc">DhcpHlprIsV4PolicySingleUC</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policyvalid">DhcpHlprIsV4PolicyValid</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policywellformed">DhcpHlprIsV4PolicyWellFormed</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprresetv4policyexpr">DhcpHlprResetV4PolicyExpr</a>