---
UID: NF:netfw.INetFwRule.put_EdgeTraversal
title: INetFwRule::put_EdgeTraversal
author: windows-driver-content
description: Indicates whether edge traversal is enabled or disabled for this rule.
old-location: ics\inetfwrule_edgetraversal.htm
old-project: ICS
ms.assetid: a45a8161-3273-4d43-86bf-34d1b776dbbc
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: EdgeTraversal property [ICS/ICF], EdgeTraversal property [ICS/ICF],INetFwRule interface, INetFwRule interface [ICS/ICF],EdgeTraversal property, INetFwRule.EdgeTraversal, INetFwRule.put_EdgeTraversal, INetFwRule::EdgeTraversal, INetFwRule::get_EdgeTraversal, INetFwRule::put_EdgeTraversal, ics.inetfwrule_edgetraversal, netfw/INetFwRule::EdgeTraversal, netfw/INetFwRule::get_EdgeTraversal, netfw/INetFwRule::put_EdgeTraversal, put_EdgeTraversal
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
-	INetFwRule.EdgeTraversal
-	INetFwRule.get_EdgeTraversal
-	INetFwRule.put_EdgeTraversal
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwRule::put_EdgeTraversal


## -description


Indicates whether edge traversal is enabled or disabled for this rule.

This property is read/write.


## -parameters


## -remarks



The EdgeTraversal property indicates that specific inbound traffic is allowed to tunnel through NATs and other edge devices using the Teredo tunneling technology.  In order for this setting to work correctly, the application or service with the inbound firewall rule needs to support IPv6.  The primary application of this setting allows listeners on the host to be globally addressable through a Teredo IPv6 address.

New rules have the EdgeTraversal property disabled by default.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

