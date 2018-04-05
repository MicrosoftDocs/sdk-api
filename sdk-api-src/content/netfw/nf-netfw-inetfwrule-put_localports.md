---
UID: NF:netfw.INetFwRule.put_LocalPorts
title: INetFwRule::put_LocalPorts method
author: windows-driver-content
description: Specifies the list of local ports for this rule.
old-location: ics\inetfwrule_localports.htm
old-project: ICS
ms.assetid: 72c4f00c-d5c4-4d93-892b-ec9a63f8df09
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ""*", "RPC", "RPC-EPMap", "Teredo", INetFwRule, INetFwRule interface [ICS/ICF], LocalPorts property, INetFwRule.LocalPorts, INetFwRule::get_LocalPorts, INetFwRule::put_LocalPorts, LocalPorts property [ICS/ICF], LocalPorts property [ICS/ICF], INetFwRule interface, ics.inetfwrule_localports, netfw/INetFwRule::LocalPorts, netfw/INetFwRule::get_LocalPorts, netfw/INetFwRule::put_LocalPorts, put_LocalPorts,INetFwRule.put_LocalPorts"
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
-	INetFwRule.LocalPorts
-	INetFwRule.get_LocalPorts
-	INetFwRule.put_LocalPorts
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# INetFwRule::put_LocalPorts method


## -description


Specifies the list of local ports for this rule.

This property is read/write.


## -parameters


## -remarks



This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.

The <a href="https://msdn.microsoft.com/library/windows/hardware/dn915742">Protocol</a> property must be set before the <b>LocalPorts</b> property or an error will be returned.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

