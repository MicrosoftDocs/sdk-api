---
UID: NS:dhcpsapi._DHCP_POL_EXPR_ARRAY
title: "_DHCP_POL_EXPR_ARRAY"
author: windows-sdk-content
description: The DHCP_POL_EXPR_ARRAY structure defines an array of DHCP server policy expressions.
old-location: dhcp\dhcp_pol_expr_array.htm
old-project: dhcp
ms.assetid: F6EDFFAC-ECBD-4B0E-A929-3DB67D8366AC
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: "*LPDHCP_POL_EXPR_ARRAY, *PDHCP_POL_EXPR_ARRAY, DHCP_POL_EXPR_ARRAY, DHCP_POL_EXPR_ARRAY structure [DHCP], LPDHCP_POL_EXPR_ARRAY, LPDHCP_POL_EXPR_ARRAY structure pointer [DHCP], PDHCP_POL_EXPR_ARRAY, PDHCP_POL_EXPR_ARRAY structure pointer [DHCP], _DHCP_POL_EXPR_ARRAY, dhcp.dhcp_pol_expr_array, dhcpsapi/DHCP_POL_EXPR_ARRAY, dhcpsapi/LPDHCP_POL_EXPR_ARRAY, dhcpsapi/PDHCP_POL_EXPR_ARRAY"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DHCP_POL_EXPR_ARRAY, *PDHCP_POL_EXPR_ARRAY, *LPDHCP_POL_EXPR_ARRAY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dhcpsapi.h
api_name:
 - DHCP_POL_EXPR_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_POL_EXPR_ARRAY structure


## -description


The <b>DHCP_POL_EXPR_ARRAY</b> structure defines an array of DHCP server policy expressions.


## -struct-fields




### -field NumElements

Integer that specifies the number of DHCP server policy expressions in <i>Elements</i>.


### -field Elements

Pointer to a list of <a href="https://msdn.microsoft.com/34e674f7-61a4-4045-9643-374f05906227">DHCP_POL_EXPR</a>  structures.


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/7e62d2f3-275a-45ab-baab-648fe135d0fc">DHCP_POLICY</a>
 

 

