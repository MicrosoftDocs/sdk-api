---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

