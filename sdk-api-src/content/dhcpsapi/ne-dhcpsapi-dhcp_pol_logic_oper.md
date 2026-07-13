---
UID: NE:dhcpsapi.DHCP_POL_LOGIC_OPER
title: DHCP_POL_LOGIC_OPER (dhcpsapi.h)
description: The DHCP_POL_LOGIC_OPER enumeration defines how to group the constituent conditions and sub-expressions of an expression in a DHCP server policy.
helpviewer_keywords: ["DHCP_POL_LOGIC_OPER","DHCP_POL_LOGIC_OPER enumeration [DHCP]","DhcpLogicalAnd","DhcpLogicalOr","dhcp.dhcp_pol_logic_oper","dhcpsapi/DHCP_POL_LOGIC_OPER","dhcpsapi/DhcpLogicalAnd","dhcpsapi/DhcpLogicalOr"]
old-location: dhcp\dhcp_pol_logic_oper.htm
tech.root: DHCP
ms.assetid: e8faffdc-2fd4-4d7a-ae9f-fd93932b8c10
ms.date: 12/05/2018
ms.keywords: DHCP_POL_LOGIC_OPER, DHCP_POL_LOGIC_OPER enumeration [DHCP], DhcpLogicalAnd, DhcpLogicalOr, dhcp.dhcp_pol_logic_oper, dhcpsapi/DHCP_POL_LOGIC_OPER, dhcpsapi/DhcpLogicalAnd, dhcpsapi/DhcpLogicalOr
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DHCP_POL_LOGIC_OPER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DHCP_POL_LOGIC_OPER
 - dhcpsapi/DHCP_POL_LOGIC_OPER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_POL_LOGIC_OPER
---

# DHCP_POL_LOGIC_OPER enumeration


## -description

The <b>DHCP_POL_LOGIC_OPER</b> enumeration defines how to group the constituent conditions and sub-expressions of an expression in a DHCP server policy.

## -enum-fields

### -field DhcpLogicalOr

The results of the constituent conditions and sub-expressions must be logically ORed to evaluate the expression.

### -field DhcpLogicalAnd

The results of the constituent conditions and sub-expressions must be logically ANDed to evaluate the expression.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_expr">DHCP_POL_EXP</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyexpr">DhcpHlprAddV4PolicyExpr</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprcreatev4policy">DhcpHlprCreateV4Policy</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprmodifyv4policyexpr">DhcpHlprModifyV4PolicyExpr</a>

