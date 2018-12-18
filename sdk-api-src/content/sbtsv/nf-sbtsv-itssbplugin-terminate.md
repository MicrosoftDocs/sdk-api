---
UID: NF:sbtsv.ITsSbPlugin.Terminate
title: ITsSbPlugin::Terminate
author: windows-sdk-content
description: Performs clean-up and unloads the plug-in.
old-location: termserv\itssbplugin_terminate.htm
tech.root: TermServ
ms.assetid: c47c6231-f967-4239-afd4-a87e9d8f49c2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbLoadBalancing interface [Remote Desktop Services],Terminate method, ITsSbLoadBalancing::Terminate, ITsSbOrchestration interface [Remote Desktop Services],Terminate method, ITsSbOrchestration::Terminate, ITsSbPlacement interface [Remote Desktop Services],Terminate method, ITsSbPlacement::Terminate, ITsSbPlugin interface [Remote Desktop Services],Terminate method, ITsSbPlugin.Terminate, ITsSbPlugin::Terminate, ITsSbProvisioning interface [Remote Desktop Services],Terminate method, ITsSbProvisioning::Terminate, ITsSbResourcePlugin interface [Remote Desktop Services],Terminate method, ITsSbResourcePlugin::Terminate, ITsSbTaskPlugin interface [Remote Desktop Services],Terminate method, ITsSbTaskPlugin::Terminate, Terminate, Terminate method [Remote Desktop Services], Terminate method [Remote Desktop Services],ITsSbLoadBalancing interface, Terminate method [Remote Desktop Services],ITsSbOrchestration interface, Terminate method [Remote Desktop Services],ITsSbPlacement interface, Terminate method [Remote Desktop Services],ITsSbPlugin interface, Terminate method [Remote Desktop Services],ITsSbProvisioning interface, Terminate method [Remote Desktop Services],ITsSbResourcePlugin interface, Terminate method [Remote Desktop Services],ITsSbTaskPlugin interface, sbtsv/ITsSbLoadBalancing::Terminate, sbtsv/ITsSbOrchestration::Terminate, sbtsv/ITsSbPlacement::Terminate, sbtsv/ITsSbPlugin::Terminate, sbtsv/ITsSbProvisioning::Terminate, sbtsv/ITsSbResourcePlugin::Terminate, sbtsv/ITsSbTaskPlugin::Terminate, termserv.itssbplugin_terminate
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbPlugin.Terminate
 - ITsSbLoadBalancing.Terminate
 - ITsSbOrchestration.Terminate
 - ITsSbPlacement.Terminate
 - ITsSbProvisioning.Terminate
 - ITsSbResourcePlugin.Terminate
 - ITsSbTaskPlugin.Terminate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbPlugin::Terminate


## -description


Performs clean-up and unloads the plug-in. Remote Desktop Connection Broker (RD Connection Broker) calls this method when it stops the RD Connection Broker service.


## -parameters




### -param hr [in]

Specifies the reason for termination. The plug-in should specify a standard <b>HRESULT</b> error code.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54">ITsSbLoadBalancing</a>



<a href="https://msdn.microsoft.com/fae858ae-19e5-453d-b9ef-1da7ea706e49">ITsSbOrchestration</a>



<a href="https://msdn.microsoft.com/d90501dd-ca15-463c-b204-b1f56103ebe7">ITsSbPlacement</a>



<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/136c1538-be4f-4b1c-b74f-8914a51f774a">ITsSbProvisioning</a>



<a href="https://msdn.microsoft.com/a5223902-2e2a-4fba-ae05-240824a140ac">ITsSbResourcePlugin</a>



<a href="https://msdn.microsoft.com/56463b47-c2f2-43b7-884f-d6fab9bebbf0">ITsSbTaskPlugin</a>
 

 

