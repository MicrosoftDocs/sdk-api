---
UID: NF:tssbx.IWTSSBPlugin.WTSSBX_GetUserExternalSession
title: IWTSSBPlugin::WTSSBX_GetUserExternalSession (tssbx.h)
description: Redirects an incoming connection to a computing resource, such as a virtual machine, a blade server, or even the user's own corporate desktop by providing a WTSSBX_MACHINE_CONNECT_INFO structure that contains information about the resource.
helpviewer_keywords: ["IWTSSBPlugin interface [Remote Desktop Services]","WTSSBX_GetUserExternalSession method","IWTSSBPlugin.WTSSBX_GetUserExternalSession","IWTSSBPlugin::WTSSBX_GetUserExternalSession","WTSSBX_GetUserExternalSession","WTSSBX_GetUserExternalSession method [Remote Desktop Services]","WTSSBX_GetUserExternalSession method [Remote Desktop Services]","IWTSSBPlugin interface","termserv.iwtssbplugin_wtssbx_getuserexternalsession","tssbx/IWTSSBPlugin::WTSSBX_GetUserExternalSession"]
old-location: termserv\iwtssbplugin_wtssbx_getuserexternalsession.htm
tech.root: TermServ
ms.assetid: 989cd7bc-932f-4a33-91c8-e66fac7195ad
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],WTSSBX_GetUserExternalSession method, IWTSSBPlugin.WTSSBX_GetUserExternalSession, IWTSSBPlugin::WTSSBX_GetUserExternalSession, WTSSBX_GetUserExternalSession, WTSSBX_GetUserExternalSession method [Remote Desktop Services], WTSSBX_GetUserExternalSession method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_wtssbx_getuserexternalsession, tssbx/IWTSSBPlugin::WTSSBX_GetUserExternalSession
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
 - IWTSSBPlugin::WTSSBX_GetUserExternalSession
 - tssbx/IWTSSBPlugin::WTSSBX_GetUserExternalSession
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
 - IWTSSBPlugin.WTSSBX_GetUserExternalSession
---

# IWTSSBPlugin::WTSSBX_GetUserExternalSession


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

Redirects an incoming connection to a computing resource, such as a virtual machine, a blade server, or even the user's own corporate desktop by providing a <a href="/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info">WTSSBX_MACHINE_CONNECT_INFO</a> structure that contains information about the resource.

## -parameters

### -param UserName [in]

A pointer to a Unicode string  that contains the user name of the incoming connection.

### -param DomainName [in]

A pointer to a Unicode string  that contains the domain name of the incoming connection.

### -param ApplicationType [in]

A pointer to a Unicode string  that contains the program that Remote Desktop Services runs after the user session is created.

### -param RedirectorInternalIP [in]

A pointer to the internal IP address of the RD Session Host server that first accepted the connection.

### -param pSessionId [out]

A pointer to the session ID of the session to which the plug-in is redirecting the incoming connection.

### -param pMachineConnectInfo [out]

A pointer to a <a href="/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info">WTSSBX_MACHINE_CONNECT_INFO</a> structure that contains information about the computer to which the plug-in  is directing the incoming connection.

## -returns

Returns <b>S_OK</b> if successful.

## -remarks

Terminal Services Session Broker (TS Session Broker) calls this method so that the plug-in can redirect an incoming connection to a computer that is not joined to a farm in TS Session Broker.

Your implementation of <b>WTSSBX_GetUserExternalSession</b> should return <b>E_NOTIMPL</b> if it does not support redirection to computers that are not joined to farms in TS Session Broker.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>