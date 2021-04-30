---
UID: NF:dhcpsapi.DhcpHlprFreeV4Policy
title: DhcpHlprFreeV4Policy function (dhcpsapi.h)
description: Frees the memory of all the data structures within a DHCP server policy structure.
helpviewer_keywords: ["DhcpHlprFreeV4Policy","DhcpHlprFreeV4Policy function [DHCP]","dhcp.dhcphlprfreev4policy","dhcpsapi/DhcpHlprFreeV4Policy"]
old-location: dhcp\dhcphlprfreev4policy.htm
tech.root: DHCP
ms.assetid: ace10974-784b-41f7-aee9-461c8d63b479
ms.date: 12/05/2018
ms.keywords: DhcpHlprFreeV4Policy, DhcpHlprFreeV4Policy function [DHCP], dhcp.dhcphlprfreev4policy, dhcpsapi/DhcpHlprFreeV4Policy
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
 - DhcpHlprFreeV4Policy
 - dhcpsapi/DhcpHlprFreeV4Policy
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
 - DhcpHlprFreeV4Policy
---

# DhcpHlprFreeV4Policy function


## -description

The <b>DhcpHlprFreeV4Policy</b> function frees the memory of all the data structures within a DHCP server policy structure.

## -parameters

### -param Policy [in, out]

Pointer to <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a> structure that contains the policy structure  to free.

## -returns

This function does not return a value.

## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyexpr">DhcpHlprAddV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyrange">DhcpHlprAddV4PolicyRange</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprcreatev4policy">DhcpHlprCreateV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policysingleuc">DhcpHlprIsV4PolicySingleUC</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policyvalid">DhcpHlprIsV4PolicyValid</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policywellformed">DhcpHlprIsV4PolicyWellFormed</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprmodifyv4policyexpr">DhcpHlprModifyV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprresetv4policyexpr">DhcpHlprResetV4PolicyExpr</a>