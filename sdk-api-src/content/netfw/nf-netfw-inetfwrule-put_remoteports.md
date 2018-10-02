---
UID: NF:netfw.INetFwRule.put_RemotePorts
title: INetFwRule::put_RemotePorts
author: windows-sdk-content
description: Specifies the list of remote ports for this rule.
old-location: ics\inetfwrule_remoteports.htm
tech.root: ICS
ms.assetid: e6791258-4669-42d9-9551-5c861bfb2b52
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: INetFwRule interface [ICS/ICF],RemotePorts property, INetFwRule.RemotePorts, INetFwRule.put_RemotePorts, INetFwRule::RemotePorts, INetFwRule::get_RemotePorts, INetFwRule::put_RemotePorts, RemotePorts property [ICS/ICF], RemotePorts property [ICS/ICF],INetFwRule interface, ics.inetfwrule_remoteports, netfw/INetFwRule::RemotePorts, netfw/INetFwRule::get_RemotePorts, netfw/INetFwRule::put_RemotePorts, put_RemotePorts
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
 - INetFwRule.RemotePorts
 - INetFwRule.get_RemotePorts
 - INetFwRule.put_RemotePorts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwRule::put_RemotePorts


## -description


Specifies the list of remote ports for this rule.

This property is read/write.


## -parameters


## -remarks



This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.

The <a href="https://msdn.microsoft.com/16f61a1d-770a-4be9-a43d-10ff9fe276fb">Protocol</a> property must be set before the <b>RemotePorts</b> property or an error will be returned.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

