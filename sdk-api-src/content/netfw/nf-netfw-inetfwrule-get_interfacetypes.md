---
UID: NF:netfw.INetFwRule.get_InterfaceTypes
title: INetFwRule::get_InterfaceTypes method
author: windows-driver-content
description: Specifies the list of interface types for which the rule applies.
old-location: ics\inetfwrule_interfacetypes.htm
old-project: ICS
ms.assetid: 2548875c-3c23-4076-9d3d-82bebf5e7718
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: INetFwRule, INetFwRule interface [ICS/ICF], InterfaceTypes property, INetFwRule.InterfaceTypes, INetFwRule::get_InterfaceTypes, INetFwRule::put_InterfaceTypes, InterfaceTypes property [ICS/ICF], InterfaceTypes property [ICS/ICF], INetFwRule interface, get_InterfaceTypes,INetFwRule.get_InterfaceTypes, ics.inetfwrule_interfacetypes, netfw/INetFwRule::InterfaceTypes, netfw/INetFwRule::get_InterfaceTypes, netfw/INetFwRule::put_InterfaceTypes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NETISO_ERROR_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FirewallAPI.dll
api_name:
-	INetFwRule.InterfaceTypes
-	INetFwRule.get_InterfaceTypes
-	INetFwRule.put_InterfaceTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INetFwRule::get_InterfaceTypes method


## -description


Specifies the list of interface types for which the rule applies.

This property is read/write.


## -parameters


## -remarks



This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.

Acceptable values for this property are "RemoteAccess", "Wireless", "Lan", and "All". If more than one interface type is specified, the strings must be separated by a comma.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

