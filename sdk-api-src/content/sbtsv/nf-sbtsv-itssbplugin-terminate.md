---
UID: NF:sbtsv.ITsSbPlugin.Terminate
title: ITsSbPlugin::Terminate (sbtsv.h)
description: Performs clean-up and unloads the plug-in.
helpviewer_keywords: ["ITsSbLoadBalancing interface [Remote Desktop Services]","Terminate method","ITsSbLoadBalancing::Terminate","ITsSbOrchestration interface [Remote Desktop Services]","Terminate method","ITsSbOrchestration::Terminate","ITsSbPlacement interface [Remote Desktop Services]","Terminate method","ITsSbPlacement::Terminate","ITsSbPlugin interface [Remote Desktop Services]","Terminate method","ITsSbPlugin.Terminate","ITsSbPlugin::Terminate","ITsSbProvisioning interface [Remote Desktop Services]","Terminate method","ITsSbProvisioning::Terminate","ITsSbResourcePlugin interface [Remote Desktop Services]","Terminate method","ITsSbResourcePlugin::Terminate","ITsSbTaskPlugin interface [Remote Desktop Services]","Terminate method","ITsSbTaskPlugin::Terminate","Terminate","Terminate method [Remote Desktop Services]","Terminate method [Remote Desktop Services]","ITsSbLoadBalancing interface","Terminate method [Remote Desktop Services]","ITsSbOrchestration interface","Terminate method [Remote Desktop Services]","ITsSbPlacement interface","Terminate method [Remote Desktop Services]","ITsSbPlugin interface","Terminate method [Remote Desktop Services]","ITsSbProvisioning interface","Terminate method [Remote Desktop Services]","ITsSbResourcePlugin interface","Terminate method [Remote Desktop Services]","ITsSbTaskPlugin interface","sbtsv/ITsSbLoadBalancing::Terminate","sbtsv/ITsSbOrchestration::Terminate","sbtsv/ITsSbPlacement::Terminate","sbtsv/ITsSbPlugin::Terminate","sbtsv/ITsSbProvisioning::Terminate","sbtsv/ITsSbResourcePlugin::Terminate","sbtsv/ITsSbTaskPlugin::Terminate","termserv.itssbplugin_terminate"]
old-location: termserv\itssbplugin_terminate.htm
tech.root: TermServ
ms.assetid: c47c6231-f967-4239-afd4-a87e9d8f49c2
ms.date: 12/05/2018
ms.keywords: ITsSbLoadBalancing interface [Remote Desktop Services],Terminate method, ITsSbLoadBalancing::Terminate, ITsSbOrchestration interface [Remote Desktop Services],Terminate method, ITsSbOrchestration::Terminate, ITsSbPlacement interface [Remote Desktop Services],Terminate method, ITsSbPlacement::Terminate, ITsSbPlugin interface [Remote Desktop Services],Terminate method, ITsSbPlugin.Terminate, ITsSbPlugin::Terminate, ITsSbProvisioning interface [Remote Desktop Services],Terminate method, ITsSbProvisioning::Terminate, ITsSbResourcePlugin interface [Remote Desktop Services],Terminate method, ITsSbResourcePlugin::Terminate, ITsSbTaskPlugin interface [Remote Desktop Services],Terminate method, ITsSbTaskPlugin::Terminate, Terminate, Terminate method [Remote Desktop Services], Terminate method [Remote Desktop Services],ITsSbLoadBalancing interface, Terminate method [Remote Desktop Services],ITsSbOrchestration interface, Terminate method [Remote Desktop Services],ITsSbPlacement interface, Terminate method [Remote Desktop Services],ITsSbPlugin interface, Terminate method [Remote Desktop Services],ITsSbProvisioning interface, Terminate method [Remote Desktop Services],ITsSbResourcePlugin interface, Terminate method [Remote Desktop Services],ITsSbTaskPlugin interface, sbtsv/ITsSbLoadBalancing::Terminate, sbtsv/ITsSbOrchestration::Terminate, sbtsv/ITsSbPlacement::Terminate, sbtsv/ITsSbPlugin::Terminate, sbtsv/ITsSbProvisioning::Terminate, sbtsv/ITsSbResourcePlugin::Terminate, sbtsv/ITsSbTaskPlugin::Terminate, termserv.itssbplugin_terminate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbPlugin::Terminate
 - sbtsv/ITsSbPlugin::Terminate
dev_langs:
 - c++
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
---

# ITsSbPlugin::Terminate


## -description

Performs clean-up and unloads the plug-in. Remote Desktop Connection Broker (RD Connection Broker) calls this method when it stops the RD Connection Broker service.

## -parameters

### -param hr [in]

Specifies the reason for termination. The plug-in should specify a standard <b>HRESULT</b> error code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing">ITsSbLoadBalancing</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration">ITsSbOrchestration</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement">ITsSbPlacement</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning">ITsSbProvisioning</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourceplugin">ITsSbResourcePlugin</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin">ITsSbTaskPlugin</a>