---
UID: NS:dhcpsapi._DHCP_POL_EXPR
title: DHCP_POL_EXPR (dhcpsapi.h)
description: The DHCP_POL_EXP structure defines a DHCP server policy expression.
helpviewer_keywords: ["*LPDHCP_POL_EXPR","*PDHCP_POL_EXPR","DHCP_POL_EXPR","DHCP_POL_EXPR structure [DHCP]","LPDHCP_POL_EXPR","LPDHCP_POL_EXPR structure pointer [DHCP]","PDHCP_POL_EXPR","PDHCP_POL_EXPR structure pointer [DHCP]","dhcp.dhcp_pol_expr","dhcpsapi/DHCP_POL_EXPR","dhcpsapi/LPDHCP_POL_EXPR","dhcpsapi/PDHCP_POL_EXPR"]
old-location: dhcp\dhcp_pol_expr.htm
tech.root: DHCP
ms.assetid: 34e674f7-61a4-4045-9643-374f05906227
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_POL_EXPR, *PDHCP_POL_EXPR, DHCP_POL_EXPR, DHCP_POL_EXPR structure [DHCP], LPDHCP_POL_EXPR, LPDHCP_POL_EXPR structure pointer [DHCP], PDHCP_POL_EXPR, PDHCP_POL_EXPR structure pointer [DHCP], dhcp.dhcp_pol_expr, dhcpsapi/DHCP_POL_EXPR, dhcpsapi/LPDHCP_POL_EXPR, dhcpsapi/PDHCP_POL_EXPR'
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
req.typenames: DHCP_POL_EXPR, *PDHCP_POL_EXPR, *LPDHCP_POL_EXPR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_POL_EXPR
 - dhcpsapi/_DHCP_POL_EXPR
 - PDHCP_POL_EXPR
 - dhcpsapi/PDHCP_POL_EXPR
 - DHCP_POL_EXPR
 - dhcpsapi/DHCP_POL_EXPR
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
 - DHCP_POL_EXPR
---

# DHCP_POL_EXPR structure


## -description

The <b>DHCP_POL_EXP</b> structure defines a DHCP server policy expression.

## -struct-fields

### -field ParentExpr

Integer that specifies the expression index that corresponds to this constituent condition.

### -field Operator

<a href="/previous-versions/windows/desktop/api/dhcpsapi/ne-dhcpsapi-dhcp_pol_logic_oper">DHCP_POL_LOGIC_OPER</a> enumeration that specifies how the results of the constituent conditions and sub-expressions must be grouped to evaluate this expression.

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a>



<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_expr_array">DHCP_POL_EXPR_ARRAY</a>