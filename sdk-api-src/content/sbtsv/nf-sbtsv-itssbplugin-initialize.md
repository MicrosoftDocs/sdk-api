---
UID: NF:sbtsv.ITsSbPlugin.Initialize
title: ITsSbPlugin::Initialize
author: windows-sdk-content
description: Initializes the plug-in.
old-location: termserv\itssbplugin_initialize.htm
old-project: TermServ
ms.assetid: 1ff0b1a2-042d-4df2-9ae4-cfa4b7c644ab
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ITsSbLoadBalancing interface [Remote Desktop Services],Initialize method, ITsSbLoadBalancing::Initialize, ITsSbOrchestration interface [Remote Desktop Services],Initialize method, ITsSbOrchestration::Initialize, ITsSbPlacement interface [Remote Desktop Services],Initialize method, ITsSbPlacement::Initialize, ITsSbPlugin interface [Remote Desktop Services],Initialize method, ITsSbPlugin.Initialize, ITsSbPlugin::Initialize, ITsSbProvisioning interface [Remote Desktop Services],Initialize method, ITsSbProvisioning::Initialize, ITsSbResourcePlugin interface [Remote Desktop Services],Initialize method, ITsSbResourcePlugin::Initialize, ITsSbTaskPlugin interface [Remote Desktop Services],Initialize method, ITsSbTaskPlugin::Initialize, Initialize, Initialize method [Remote Desktop Services], Initialize method [Remote Desktop Services],ITsSbLoadBalancing interface, Initialize method [Remote Desktop Services],ITsSbOrchestration interface, Initialize method [Remote Desktop Services],ITsSbPlacement interface, Initialize method [Remote Desktop Services],ITsSbPlugin interface, Initialize method [Remote Desktop Services],ITsSbProvisioning interface, Initialize method [Remote Desktop Services],ITsSbResourcePlugin interface, Initialize method [Remote Desktop Services],ITsSbTaskPlugin interface, sbtsv/ITsSbLoadBalancing::Initialize, sbtsv/ITsSbOrchestration::Initialize, sbtsv/ITsSbPlacement::Initialize, sbtsv/ITsSbPlugin::Initialize, sbtsv/ITsSbProvisioning::Initialize, sbtsv/ITsSbResourcePlugin::Initialize, sbtsv/ITsSbTaskPlugin::Initialize, termserv.itssbplugin_initialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbPlugin.Initialize
 - ITsSbLoadBalancing.Initialize
 - ITsSbOrchestration.Initialize
 - ITsSbPlacement.Initialize
 - ITsSbProvisioning.Initialize
 - ITsSbResourcePlugin.Initialize
 - ITsSbTaskPlugin.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITsSbPlugin::Initialize


## -description


Initializes the plug-in.

Remote Desktop Connection Broker (RD Connection Broker) calls this method immediately after the RD Connection Broker service starts. Plug-ins can use this method to add information about existing environments and targets in the RD Connection Broker store.


<a href="https://msdn.microsoft.com/a5223902-2e2a-4fba-ae05-240824a140ac">ITsSbResourcePlugin</a>
<a href="https://msdn.microsoft.com/2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54">ITsSbLoadBalancing</a>
<a href="https://msdn.microsoft.com/d90501dd-ca15-463c-b204-b1f56103ebe7">ITsSbPlacement</a>
<a href="https://msdn.microsoft.com/fae858ae-19e5-453d-b9ef-1da7ea706e49">ITsSbOrchestration</a>
<a href="https://msdn.microsoft.com/56463b47-c2f2-43b7-884f-d6fab9bebbf0">ITsSbTaskPlugin</a>



## -parameters




### -param pProvider [in]

A pointer to an <a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a> provider object. 


### -param pNotifySink [in]

A pointer to an <a href="https://msdn.microsoft.com/c52a3253-74cb-4ff9-a4f3-cb9601c02e7d">ITsSbPluginNotifySink</a> notify sink object. 


### -param pPropertySet [in]

A pointer to an <a href="https://msdn.microsoft.com/e28e4ce7-1d11-483e-b666-69b3c0ba34b1">ITsSbPluginPropertySet</a> plug-in property set object. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins should call <a href="https://msdn.microsoft.com/2fe468c9-457f-4a56-aaf9-4eb48fec8720">OnInitialized</a> on the specified <a href="https://msdn.microsoft.com/c52a3253-74cb-4ff9-a4f3-cb9601c02e7d">ITsSbPluginNotifySink</a> sink object.




## -see-also




<a href="https://msdn.microsoft.com/2dc9dd37-0dc1-4b73-bcac-9fb3d1158b54">ITsSbLoadBalancing</a>



<a href="https://msdn.microsoft.com/fae858ae-19e5-453d-b9ef-1da7ea706e49">ITsSbOrchestration</a>



<a href="https://msdn.microsoft.com/d90501dd-ca15-463c-b204-b1f56103ebe7">ITsSbPlacement</a>



<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/c52a3253-74cb-4ff9-a4f3-cb9601c02e7d">ITsSbPluginNotifySink</a>



<a href="https://msdn.microsoft.com/e28e4ce7-1d11-483e-b666-69b3c0ba34b1">ITsSbPluginPropertySet</a>



<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>



<a href="https://msdn.microsoft.com/136c1538-be4f-4b1c-b74f-8914a51f774a">ITsSbProvisioning</a>



<a href="https://msdn.microsoft.com/a5223902-2e2a-4fba-ae05-240824a140ac">ITsSbResourcePlugin</a>



<a href="https://msdn.microsoft.com/56463b47-c2f2-43b7-884f-d6fab9bebbf0">ITsSbTaskPlugin</a>
 

 

