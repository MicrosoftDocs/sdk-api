---
UID: NF:sbtsv.ITsSbPlugin.Initialize
title: ITsSbPlugin::Initialize (sbtsv.h)
description: Initializes the plug-in.
helpviewer_keywords: ["ITsSbLoadBalancing interface [Remote Desktop Services]","Initialize method","ITsSbLoadBalancing::Initialize","ITsSbOrchestration interface [Remote Desktop Services]","Initialize method","ITsSbOrchestration::Initialize","ITsSbPlacement interface [Remote Desktop Services]","Initialize method","ITsSbPlacement::Initialize","ITsSbPlugin interface [Remote Desktop Services]","Initialize method","ITsSbPlugin.Initialize","ITsSbPlugin::Initialize","ITsSbProvisioning interface [Remote Desktop Services]","Initialize method","ITsSbProvisioning::Initialize","ITsSbResourcePlugin interface [Remote Desktop Services]","Initialize method","ITsSbResourcePlugin::Initialize","ITsSbTaskPlugin interface [Remote Desktop Services]","Initialize method","ITsSbTaskPlugin::Initialize","Initialize","Initialize method [Remote Desktop Services]","Initialize method [Remote Desktop Services]","ITsSbLoadBalancing interface","Initialize method [Remote Desktop Services]","ITsSbOrchestration interface","Initialize method [Remote Desktop Services]","ITsSbPlacement interface","Initialize method [Remote Desktop Services]","ITsSbPlugin interface","Initialize method [Remote Desktop Services]","ITsSbProvisioning interface","Initialize method [Remote Desktop Services]","ITsSbResourcePlugin interface","Initialize method [Remote Desktop Services]","ITsSbTaskPlugin interface","sbtsv/ITsSbLoadBalancing::Initialize","sbtsv/ITsSbOrchestration::Initialize","sbtsv/ITsSbPlacement::Initialize","sbtsv/ITsSbPlugin::Initialize","sbtsv/ITsSbProvisioning::Initialize","sbtsv/ITsSbResourcePlugin::Initialize","sbtsv/ITsSbTaskPlugin::Initialize","termserv.itssbplugin_initialize"]
old-location: termserv\itssbplugin_initialize.htm
tech.root: TermServ
ms.assetid: 1ff0b1a2-042d-4df2-9ae4-cfa4b7c644ab
ms.date: 12/05/2018
ms.keywords: ITsSbLoadBalancing interface [Remote Desktop Services],Initialize method, ITsSbLoadBalancing::Initialize, ITsSbOrchestration interface [Remote Desktop Services],Initialize method, ITsSbOrchestration::Initialize, ITsSbPlacement interface [Remote Desktop Services],Initialize method, ITsSbPlacement::Initialize, ITsSbPlugin interface [Remote Desktop Services],Initialize method, ITsSbPlugin.Initialize, ITsSbPlugin::Initialize, ITsSbProvisioning interface [Remote Desktop Services],Initialize method, ITsSbProvisioning::Initialize, ITsSbResourcePlugin interface [Remote Desktop Services],Initialize method, ITsSbResourcePlugin::Initialize, ITsSbTaskPlugin interface [Remote Desktop Services],Initialize method, ITsSbTaskPlugin::Initialize, Initialize, Initialize method [Remote Desktop Services], Initialize method [Remote Desktop Services],ITsSbLoadBalancing interface, Initialize method [Remote Desktop Services],ITsSbOrchestration interface, Initialize method [Remote Desktop Services],ITsSbPlacement interface, Initialize method [Remote Desktop Services],ITsSbPlugin interface, Initialize method [Remote Desktop Services],ITsSbProvisioning interface, Initialize method [Remote Desktop Services],ITsSbResourcePlugin interface, Initialize method [Remote Desktop Services],ITsSbTaskPlugin interface, sbtsv/ITsSbLoadBalancing::Initialize, sbtsv/ITsSbOrchestration::Initialize, sbtsv/ITsSbPlacement::Initialize, sbtsv/ITsSbPlugin::Initialize, sbtsv/ITsSbProvisioning::Initialize, sbtsv/ITsSbResourcePlugin::Initialize, sbtsv/ITsSbTaskPlugin::Initialize, termserv.itssbplugin_initialize
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
 - ITsSbPlugin::Initialize
 - sbtsv/ITsSbPlugin::Initialize
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
 - ITsSbPlugin.Initialize
 - ITsSbLoadBalancing.Initialize
 - ITsSbOrchestration.Initialize
 - ITsSbPlacement.Initialize
 - ITsSbProvisioning.Initialize
 - ITsSbResourcePlugin.Initialize
 - ITsSbTaskPlugin.Initialize
---

# ITsSbPlugin::Initialize


## -description

Initializes the plug-in.

Remote Desktop Connection Broker (RD Connection Broker) calls this method immediately after the RD Connection Broker service starts. Plug-ins can use this method to add information about existing environments and targets in the RD Connection Broker store.


<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourceplugin">ITsSbResourcePlugin</a>
<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing">ITsSbLoadBalancing</a>
<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement">ITsSbPlacement</a>
<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration">ITsSbOrchestration</a>
<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin">ITsSbTaskPlugin</a>

## -parameters

### -param pProvider [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a> provider object.

### -param pNotifySink [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink">ITsSbPluginNotifySink</a> notify sink object.

### -param pPropertySet [in]

A pointer to an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginpropertyset">ITsSbPluginPropertySet</a> plug-in property set object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Plug-ins should call <a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbpluginnotifysink-oninitialized">OnInitialized</a> on the specified <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink">ITsSbPluginNotifySink</a> sink object.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing">ITsSbLoadBalancing</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration">ITsSbOrchestration</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement">ITsSbPlacement</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink">ITsSbPluginNotifySink</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginpropertyset">ITsSbPluginPropertySet</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning">ITsSbProvisioning</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourceplugin">ITsSbResourcePlugin</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin">ITsSbTaskPlugin</a>