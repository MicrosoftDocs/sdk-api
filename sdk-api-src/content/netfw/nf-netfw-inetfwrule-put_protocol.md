---
UID: NF:netfw.INetFwRule.put_Protocol
title: INetFwRule::put_Protocol
author: windows-sdk-content
description: Specifies the IP protocol of this rule.
old-location: ics\inetfwrule_protocol.htm
tech.root: ics
ms.assetid: 16f61a1d-770a-4be9-a43d-10ff9fe276fb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetFwRule interface [ICS/ICF],Protocol property, INetFwRule.Protocol, INetFwRule.put_Protocol, INetFwRule::Protocol, INetFwRule::get_Protocol, INetFwRule::put_Protocol, Protocol property [ICS/ICF], Protocol property [ICS/ICF],INetFwRule interface, ics.inetfwrule_protocol, netfw/INetFwRule::Protocol, netfw/INetFwRule::get_Protocol, netfw/INetFwRule::put_Protocol, put_Protocol
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
 - INetFwRule.Protocol
 - INetFwRule.get_Protocol
 - INetFwRule.put_Protocol
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwRule::put_Protocol


## -description


Specifies the IP protocol  of this rule.

This property is read/write.


## -parameters


## -remarks



This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.

The <b>Protocol</b> property must be set before the <a href="https://msdn.microsoft.com/72c4f00c-d5c4-4d93-892b-ec9a63f8df09">LocalPorts</a> or <a href="https://msdn.microsoft.com/e6791258-4669-42d9-9551-5c861bfb2b52">RemotePorts</a> properties or an error will be returned.

A list of protocol numbers is available at the  <a href="http://go.microsoft.com/fwlink/p/?linkid=89889">IANA website</a>.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

