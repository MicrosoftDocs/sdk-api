---
UID: NF:netfw.INetFwPolicy2.get_DefaultInboundAction
title: INetFwPolicy2::get_DefaultInboundAction
author: windows-sdk-content
description: Specifies the default action for inbound traffic. These settings are Block by default.
old-location: ics\inetfwpolicy2_defaultinboundaction.htm
tech.root: ics
ms.assetid: d9251979-0479-4245-8a29-a161acbf591f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DefaultInboundAction property [ICS/ICF], DefaultInboundAction property [ICS/ICF],INetFwPolicy2 interface, INetFwPolicy2 interface [ICS/ICF],DefaultInboundAction property, INetFwPolicy2.DefaultInboundAction, INetFwPolicy2.get_DefaultInboundAction, INetFwPolicy2::DefaultInboundAction, INetFwPolicy2::get_DefaultInboundAction, INetFwPolicy2::put_DefaultInboundAction, get_DefaultInboundAction, ics.inetfwpolicy2_defaultinboundaction, netfw/INetFwPolicy2::DefaultInboundAction, netfw/INetFwPolicy2::get_DefaultInboundAction, netfw/INetFwPolicy2::put_DefaultInboundAction
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
 - INetFwPolicy2.DefaultInboundAction
 - INetFwPolicy2.get_DefaultInboundAction
 - INetFwPolicy2.put_DefaultInboundAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwPolicy2::get_DefaultInboundAction


## -description


Specifies the default action for inbound traffic. These settings are Block by default.

This property is read/write.


## -parameters


## -remarks



All interfaces are firewall-enabled. This means that all the exceptions (such as GloballyOpenPorts, Applications, or Services) which are  specified in the profile, are ignored
   and only locally-initiated traffic is allowed.

When you pass a profile type obtained from the <a href="https://msdn.microsoft.com/93f4b508-30db-45a9-a7aa-df4a993dc50b">CurrentProfileTypes</a> property, make sure that you pass only one profile type to <b>get_DefaultInboundAction</b> and <b>put_DefaultInboundAction</b>. Note that <b>get_CurrentProfileTypes</b> can return multiple profiles.




## -see-also




<a href="https://msdn.microsoft.com/ef01a531-ddb0-4eb4-894b-82f613016396">INetFwPolicy2</a>



<a href="https://msdn.microsoft.com/1120e802-9159-450b-bee2-700e49d4fa61">NET_FW_ACTION</a>



<a href="https://msdn.microsoft.com/cb8328ec-a2eb-4d6f-b6af-214a31a037e9">NET_FW_PROFILE_TYPE2</a>
 

 

