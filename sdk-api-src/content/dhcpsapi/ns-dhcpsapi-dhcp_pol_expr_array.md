---
UID: NS:dhcpsapi._DHCP_POL_EXPR_ARRAY
title: DHCP_POL_EXPR_ARRAY (dhcpsapi.h)
description: The DHCP_POL_EXPR_ARRAY structure defines an array of DHCP server policy expressions.
helpviewer_keywords: ["*LPDHCP_POL_EXPR_ARRAY","*PDHCP_POL_EXPR_ARRAY","DHCP_POL_EXPR_ARRAY","DHCP_POL_EXPR_ARRAY structure [DHCP]","LPDHCP_POL_EXPR_ARRAY","LPDHCP_POL_EXPR_ARRAY structure pointer [DHCP]","PDHCP_POL_EXPR_ARRAY","PDHCP_POL_EXPR_ARRAY structure pointer [DHCP]","dhcp.dhcp_pol_expr_array","dhcpsapi/DHCP_POL_EXPR_ARRAY","dhcpsapi/LPDHCP_POL_EXPR_ARRAY","dhcpsapi/PDHCP_POL_EXPR_ARRAY"]
old-location: dhcp\dhcp_pol_expr_array.htm
tech.root: DHCP
ms.assetid: F6EDFFAC-ECBD-4B0E-A929-3DB67D8366AC
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_POL_EXPR_ARRAY, *PDHCP_POL_EXPR_ARRAY, DHCP_POL_EXPR_ARRAY, DHCP_POL_EXPR_ARRAY structure [DHCP], LPDHCP_POL_EXPR_ARRAY, LPDHCP_POL_EXPR_ARRAY structure pointer [DHCP], PDHCP_POL_EXPR_ARRAY, PDHCP_POL_EXPR_ARRAY structure pointer [DHCP], dhcp.dhcp_pol_expr_array, dhcpsapi/DHCP_POL_EXPR_ARRAY, dhcpsapi/LPDHCP_POL_EXPR_ARRAY, dhcpsapi/PDHCP_POL_EXPR_ARRAY'
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
req.typenames: DHCP_POL_EXPR_ARRAY, *PDHCP_POL_EXPR_ARRAY, *LPDHCP_POL_EXPR_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_POL_EXPR_ARRAY
 - dhcpsapi/_DHCP_POL_EXPR_ARRAY
 - PDHCP_POL_EXPR_ARRAY
 - dhcpsapi/PDHCP_POL_EXPR_ARRAY
 - DHCP_POL_EXPR_ARRAY
 - dhcpsapi/DHCP_POL_EXPR_ARRAY
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
 - DHCP_POL_EXPR_ARRAY
---

# DHCP_POL_EXPR_ARRAY structure


## -description

The <b>DHCP_POL_EXPR_ARRAY</b> structure defines an array of DHCP server policy expressions.

## -struct-fields

### -field NumElements

Integer that specifies the number of DHCP server policy expressions in <i>Elements</i>.

### -field Elements

Pointer to a list of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_pol_expr">DHCP_POL_EXPR</a>  structures.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_policy">DHCP_POLICY</a>