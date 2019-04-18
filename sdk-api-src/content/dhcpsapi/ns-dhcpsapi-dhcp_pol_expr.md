---
UID: NS:dhcpsapi._DHCP_POL_EXPR
title: DHCP_POL_EXPR (dhcpsapi.h)
author: windows-sdk-content
description: The DHCP_POL_EXP structure defines a DHCP server policy expression.
old-location: dhcp\dhcp_pol_expr.htm
tech.root: DHCP
ms.assetid: 34e674f7-61a4-4045-9643-374f05906227
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPDHCP_POL_EXPR, *PDHCP_POL_EXPR, DHCP_POL_EXPR, DHCP_POL_EXPR structure [DHCP], LPDHCP_POL_EXPR, LPDHCP_POL_EXPR structure pointer [DHCP], PDHCP_POL_EXPR, PDHCP_POL_EXPR structure pointer [DHCP], dhcp.dhcp_pol_expr, dhcpsapi/DHCP_POL_EXPR, dhcpsapi/LPDHCP_POL_EXPR, dhcpsapi/PDHCP_POL_EXPR"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_POL_EXPR
product: Windows
targetos: Windows
req.typenames: DHCP_POL_EXPR, *PDHCP_POL_EXPR, *LPDHCP_POL_EXPR
req.redist: 
ms.custom: 19H1
---

# DHCP_POL_EXPR structure


## -description


The <b>DHCP_POL_EXP</b> structure defines a DHCP server policy expression.


## -struct-fields




### -field ParentExpr

Integer that specifies the expression index that corresponds to this constituent condition.


### -field Operator


<a href="https://msdn.microsoft.com/e8faffdc-2fd4-4d7a-ae9f-fd93932b8c10">DHCP_POL_LOGIC_OPER</a> enumeration that specifies how the results of the constituent conditions and sub-expressions must be grouped to evaluate this expression.


## -see-also




<a href="https://msdn.microsoft.com/7e62d2f3-275a-45ab-baab-648fe135d0fc">DHCP_POLICY</a>



<a href="https://msdn.microsoft.com/F6EDFFAC-ECBD-4B0E-A929-3DB67D8366AC">DHCP_POL_EXPR_ARRAY</a>
 

 

