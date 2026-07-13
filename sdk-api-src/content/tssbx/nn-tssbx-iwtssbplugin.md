---
UID: NN:tssbx.IWTSSBPlugin
title: IWTSSBPlugin (tssbx.h)
description: Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker). Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.
helpviewer_keywords: ["IWTSSBPlugin","IWTSSBPlugin interface [Remote Desktop Services]","IWTSSBPlugin interface [Remote Desktop Services]","described","termserv.iwtssbplugin","tssbx/IWTSSBPlugin"]
old-location: termserv\iwtssbplugin.htm
tech.root: TermServ
ms.assetid: f6959b8c-a8a8-438b-8b6d-31bf0e782bac
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin, IWTSSBPlugin interface [Remote Desktop Services], IWTSSBPlugin interface [Remote Desktop Services],described, termserv.iwtssbplugin, tssbx/IWTSSBPlugin
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
 - IWTSSBPlugin
 - tssbx/IWTSSBPlugin
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
 - IWTSSBPlugin
---

# IWTSSBPlugin interface


## -description

<p class="CCE_Message">[The <b>IWTSSBPlugin</b> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).  Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.

## -inheritance

The <b>IWTSSBPlugin</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWTSSBPlugin</b> also has these types of members:

## -remarks

TS Session Broker calls the <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getuserexternalsession">WTSSBX_GetUserExternalSession</a> method so that the plug-in can direct an incoming connection to a computer that does not belong to a farm in TS Session Broker.

Alternatively, TS Session Broker calls the <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getmostsuitableserver">WTSSBX_GetMostSuitableServer</a> method so that the plug-in can direct an incoming connection to a computer that does belong to a farm in TS Session Broker.

These methods reference an individual server in the farm by using the unique <i>MachineId</i> assigned to the server by TS Session Broker. When a server joins a farm in TS Session Broker, TS Session Broker calls the <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_machinechangenotification">WTSSBX_MachineChangeNotification</a> method to notify the plug-in of the change and pass the <i>MachineId</i> of the new server to the plug-in.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/TermServ/extending-ts-session-broker">Remote Desktop Connection Broker Extensibility</a>
