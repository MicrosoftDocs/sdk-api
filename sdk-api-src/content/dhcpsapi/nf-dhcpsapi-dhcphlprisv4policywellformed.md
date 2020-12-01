---
UID: NF:dhcpsapi.DhcpHlprIsV4PolicyWellFormed
title: DhcpHlprIsV4PolicyWellFormed function (dhcpsapi.h)
description: Verifies that a DHCP server policy structure is well formed.
helpviewer_keywords: ["DhcpHlprIsV4PolicyWellFormed","DhcpHlprIsV4PolicyWellFormed function [DHCP]","dhcp.dhcphlprisv4policywellformed","dhcpsapi/DhcpHlprIsV4PolicyWellFormed"]
old-location: dhcp\dhcphlprisv4policywellformed.htm
tech.root: DHCP
ms.assetid: 820b45f6-aa09-4e15-bf77-caa2723f4ea8
ms.date: 12/05/2018
ms.keywords: DhcpHlprIsV4PolicyWellFormed, DhcpHlprIsV4PolicyWellFormed function [DHCP], dhcp.dhcphlprisv4policywellformed, dhcpsapi/DhcpHlprIsV4PolicyWellFormed
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
 - DhcpHlprIsV4PolicyWellFormed
 - dhcpsapi/DhcpHlprIsV4PolicyWellFormed
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
 - DhcpHlprIsV4PolicyWellFormed
---

# DhcpHlprIsV4PolicyWellFormed function


## -description

The <b>DhcpHlprIsV4PolicyWellFormed</b> function verifies that a DHCP server policy structure is well formed.

## -parameters

### -param pPolicy [in]

Pointer to <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the policy to verify

## -returns

The API returns <b>TRUE</b> if the specified policy satisfies the conditions in the <b>Remarks</b> below. Otherwise, it returns <b>FALSE</b>.

## -remarks

The API performs the following validations on the policy conditions and expression structure.


<ol>
<li>Every clause in the policy condition must have a valid parent expression.</li>
<li>Every expression in the policy structure must have conditions or other expressions as children.</li>
<li>Only one expression must be the root expression.</li>
<li>All non-root expressions must have valid parent expression.</li>
<li>There must be no cyclic relationship between the expressions. Each expression must have the parent expression index lesser than that of itself.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyexpr">DhcpHlprAddV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyrange">DhcpHlprAddV4PolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprcreatev4policy">DhcpHlprCreateV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprfreev4policy">DhcpHlprFreeV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policysingleuc">DhcpHlprIsV4PolicySingleUC</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policyvalid">DhcpHlprIsV4PolicyValid</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprmodifyv4policyexpr">DhcpHlprModifyV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprresetv4policyexpr">DhcpHlprResetV4PolicyExpr</a>