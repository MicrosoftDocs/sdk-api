---
UID: NF:tssbx.IWTSSBPlugin.Initialize
title: IWTSSBPlugin::Initialize (tssbx.h)
description: Initializes the plug-in and returns a value that indicates the redirection capabilities of the plug-in.
helpviewer_keywords: ["IWTSSBPlugin interface [Remote Desktop Services]","Initialize method","IWTSSBPlugin.Initialize","IWTSSBPlugin::Initialize","Initialize","Initialize method [Remote Desktop Services]","Initialize method [Remote Desktop Services]","IWTSSBPlugin interface","termserv.iwtssbplugin_initialize","tssbx/IWTSSBPlugin::Initialize"]
old-location: termserv\iwtssbplugin_initialize.htm
tech.root: TermServ
ms.assetid: b9304f4a-49ed-4a5e-87a1-7a9bc1c01b3d
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],Initialize method, IWTSSBPlugin.Initialize, IWTSSBPlugin::Initialize, Initialize, Initialize method [Remote Desktop Services], Initialize method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_initialize, tssbx/IWTSSBPlugin::Initialize
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
 - IWTSSBPlugin::Initialize
 - tssbx/IWTSSBPlugin::Initialize
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
 - IWTSSBPlugin.Initialize
---

# IWTSSBPlugin::Initialize


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

Initializes the plug-in and returns a value that indicates the redirection capabilities of the 
    plug-in. Terminal Services Session Broker (TS Session Broker) calls this method 
    immediately after it instantiates the plug-in class.

## -parameters

### -param PluginCapabilities [out]

A pointer to a value that indicates the redirection capabilities of the plug-in.



#### 0

The plug-in redirects only within a farm in TS Session Broker. If this value is returned, TS Session Broker does not call the <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getuserexternalsession">WTSSBX_GetUserExternalSession</a> method on the plug-in.



#### 1

The plug-in redirects within a farm in TS Session Broker, and the plug-in implements <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_getuserexternalsession">WTSSBX_GetUserExternalSession</a> to redirect outside the farm.

## -returns

Returns <b>S_OK</b> if successful.

## -remarks

TS Session Broker calls <b>Initialize</b> immediately after it instantiates the COM class. The plug-in should return information about its redirection capabilities  by using the <b>Initialize</b> method.

Your implementation of <b>Initialize</b> must return <b>S_OK</b> immediately if successful.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>