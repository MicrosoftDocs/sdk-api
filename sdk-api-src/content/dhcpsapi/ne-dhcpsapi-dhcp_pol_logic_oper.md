---
UID: NE:dhcpsapi.__unnamed_enum_4
title: DHCP_POL_LOGIC_OPER
author: windows-sdk-content
description: The DHCP_POL_LOGIC_OPER enumeration defines how to group the constituent conditions and sub-expressions of an expression in a DHCP server policy.
old-location: dhcp\dhcp_pol_logic_oper.htm
tech.root: DHCP
ms.assetid: e8faffdc-2fd4-4d7a-ae9f-fd93932b8c10
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DHCP_POL_LOGIC_OPER, DHCP_POL_LOGIC_OPER enumeration [DHCP], DhcpLogicalAnd, DhcpLogicalOr, dhcp.dhcp_pol_logic_oper, dhcpsapi/DHCP_POL_LOGIC_OPER, dhcpsapi/DhcpLogicalAnd, dhcpsapi/DhcpLogicalOr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - DHCP_POL_LOGIC_OPER
product: Windows
targetos: Windows
req.typenames: DHCP_POL_LOGIC_OPER
req.redist: 
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




<a href="https://msdn.microsoft.com/34e674f7-61a4-4045-9643-374f05906227">DHCP_POL_EXP</a>



<a href="https://msdn.microsoft.com/549d86ed-81c1-4126-9f43-f7e5340990d3">DhcpHlprAddV4PolicyExpr</a>



<a href="https://msdn.microsoft.com/91f04578-9f15-44b4-8cf6-99be13d0395e">DhcpHlprCreateV4Policy</a>



<a href="https://msdn.microsoft.com/5d6818f9-4e44-4f24-a489-84defd1117c0">DhcpHlprModifyV4PolicyExpr</a>
 

 

