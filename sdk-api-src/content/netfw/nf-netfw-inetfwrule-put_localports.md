---
UID: NF:netfw.INetFwRule.put_LocalPorts
title: INetFwRule::put_LocalPorts
author: windows-sdk-content
description: Specifies the list of local ports for this rule.
old-location: ics\inetfwrule_localports.htm
tech.root: ics
ms.assetid: 72c4f00c-d5c4-4d93-892b-ec9a63f8df09
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ""*", "RPC", "RPC-EPMap", "Teredo", INetFwRule interface [ICS/ICF],LocalPorts property, INetFwRule.LocalPorts, INetFwRule.put_LocalPorts, INetFwRule::LocalPorts, INetFwRule::get_LocalPorts, INetFwRule::put_LocalPorts, LocalPorts property [ICS/ICF], LocalPorts property [ICS/ICF],INetFwRule interface, ics.inetfwrule_localports, netfw/INetFwRule::LocalPorts, netfw/INetFwRule::get_LocalPorts, netfw/INetFwRule::put_LocalPorts, put_LocalPorts"
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
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule.LocalPorts
 - INetFwRule.get_LocalPorts
 - INetFwRule.put_LocalPorts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwRule::put_LocalPorts


## -description


Specifies the list of local ports for this rule.

This property is read/write.


## -parameters


## -remarks



This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.

The <a href="https://msdn.microsoft.com/16f61a1d-770a-4be9-a43d-10ff9fe276fb">Protocol</a> property must be set before the <b>LocalPorts</b> property or an error will be returned.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

