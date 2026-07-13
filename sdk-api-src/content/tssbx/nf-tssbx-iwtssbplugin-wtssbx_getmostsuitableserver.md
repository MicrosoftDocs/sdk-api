---
UID: NF:tssbx.IWTSSBPlugin.WTSSBX_GetMostSuitableServer
title: IWTSSBPlugin::WTSSBX_GetMostSuitableServer (tssbx.h)
description: Returns the ID of the server to which Terminal Services Session Broker (TS Session Broker) should direct the incoming connection.
helpviewer_keywords: ["IWTSSBPlugin interface [Remote Desktop Services]","WTSSBX_GetMostSuitableServer method","IWTSSBPlugin.WTSSBX_GetMostSuitableServer","IWTSSBPlugin::WTSSBX_GetMostSuitableServer","WTSSBX_GetMostSuitableServer","WTSSBX_GetMostSuitableServer method [Remote Desktop Services]","WTSSBX_GetMostSuitableServer method [Remote Desktop Services]","IWTSSBPlugin interface","termserv.iwtssbplugin_wtssbx_getmostsuitableserver","tssbx/IWTSSBPlugin::WTSSBX_GetMostSuitableServer"]
old-location: termserv\iwtssbplugin_wtssbx_getmostsuitableserver.htm
tech.root: TermServ
ms.assetid: d25527ec-1007-4b7b-93ad-6c96780dddec
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],WTSSBX_GetMostSuitableServer method, IWTSSBPlugin.WTSSBX_GetMostSuitableServer, IWTSSBPlugin::WTSSBX_GetMostSuitableServer, WTSSBX_GetMostSuitableServer, WTSSBX_GetMostSuitableServer method [Remote Desktop Services], WTSSBX_GetMostSuitableServer method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_wtssbx_getmostsuitableserver, tssbx/IWTSSBPlugin::WTSSBX_GetMostSuitableServer
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
 - IWTSSBPlugin::WTSSBX_GetMostSuitableServer
 - tssbx/IWTSSBPlugin::WTSSBX_GetMostSuitableServer
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
 - IWTSSBPlugin.WTSSBX_GetMostSuitableServer
---

# IWTSSBPlugin::WTSSBX_GetMostSuitableServer


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

Returns the ID of the server to which Terminal Services Session Broker (TS Session Broker) should direct the incoming connection. The  redirection logic of  the plug-in determines the preferred server.

## -parameters

### -param UserName [in]

A pointer to a Unicode string that contains the user name of the incoming connection.

### -param DomainName [in]

A pointer to a Unicode string that contains the domain name that is associated with the  incoming connection.

### -param ApplicationType [in]

A pointer to a Unicode string that contains the name of the program that Remote Desktop Services runs after it creates the session.

### -param FarmName [in]

A pointer to a Unicode string that contains the name of the farm in TS Session Broker that the user is connecting to.

### -param pMachineId [in, out]

A pointer to the ID of the server to which TS Session Broker will redirect the incoming connection.  This value is initially set to the  ID of the server provided by the load balancing logic of TS Session Broker.

## -returns

Returns <b>S_OK</b> if successful.

## -remarks

Use <b>WTSSBX_GetMostSuitableServer</b>  to override the default load balancing logic of TS Session Broker. TS Session Broker calls this method after it runs its own load balancing logic. The <i>pMachineId</i>  parameter is initially set to the ID of the server provided by the load balancing logic of TS Session Broker. When you implement this method, your redirection logic can return this <i>pMachineId</i> or another one as appropriate.

Whenever a server joins a farm in TS Session Broker, TS Session Broker calls the <a href="/windows/desktop/api/tssbx/nf-tssbx-iwtssbplugin-wtssbx_machinechangenotification">WTSSBX_MachineChangeNotification</a> method to notify the plug-in and provide a MachineId to identify the new server. When TS Session Broker calls <b>WTSSBX_GetMostSuitableServer</b>, the plug-in should return one of the IDs that TS Session Broker provided to the plug-in.  The plug-in should not return the ID of a server that is not in the farm.

Your implementation of <b>WTSSBX_GetMostSuitableServer</b> must return <b>S_OK</b> immediately if successful.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>