---
UID: NF:tssbx.IWTSSBPlugin.Terminated
title: IWTSSBPlugin::Terminated (tssbx.h)
description: Notifies the plug-in that it is about to be destroyed by Terminal Services Session Broker (TS Session Broker).
helpviewer_keywords: ["IWTSSBPlugin interface [Remote Desktop Services]","Terminated method","IWTSSBPlugin.Terminated","IWTSSBPlugin::Terminated","Terminated","Terminated method [Remote Desktop Services]","Terminated method [Remote Desktop Services]","IWTSSBPlugin interface","termserv.iwtssbplugin_terminated","tssbx/IWTSSBPlugin::Terminated"]
old-location: termserv\iwtssbplugin_terminated.htm
tech.root: TermServ
ms.assetid: 123455dd-6ef3-409f-b021-e641868b16f0
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],Terminated method, IWTSSBPlugin.Terminated, IWTSSBPlugin::Terminated, Terminated, Terminated method [Remote Desktop Services], Terminated method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_terminated, tssbx/IWTSSBPlugin::Terminated
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
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
 - IWTSSBPlugin::Terminated
 - tssbx/IWTSSBPlugin::Terminated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tssbx.h
api_name:
 - IWTSSBPlugin.Terminated
---

# IWTSSBPlugin::Terminated


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

 Notifies the plug-in that it is about to be destroyed by Terminal Services Session Broker (TS Session Broker).



## -returns

Returns <b>S_OK</b> if successful.

## -remarks

TS Session Broker calls this method before it destroys this instance of the plug-in. You can use this method to perform cleanup for the plug-in before TS Session Broker destroys it. After the plug-in is destroyed, TS Session Broker reverts to its native redirection service.

Your implementation of this method must return <b>S_OK</b> immediately if successful.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>
