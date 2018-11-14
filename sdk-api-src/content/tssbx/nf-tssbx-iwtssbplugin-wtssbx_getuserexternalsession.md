---
UID: NF:tssbx.IWTSSBPlugin.WTSSBX_GetUserExternalSession
title: IWTSSBPlugin::WTSSBX_GetUserExternalSession
author: windows-sdk-content
description: Redirects an incoming connection to a computing resource, such as a virtual machine, a blade server, or even the user's own corporate desktop by providing a WTSSBX_MACHINE_CONNECT_INFO structure that contains information about the resource.
old-location: termserv\iwtssbplugin_wtssbx_getuserexternalsession.htm
tech.root: termserv
ms.assetid: 989cd7bc-932f-4a33-91c8-e66fac7195ad
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],WTSSBX_GetUserExternalSession method, IWTSSBPlugin.WTSSBX_GetUserExternalSession, IWTSSBPlugin::WTSSBX_GetUserExternalSession, WTSSBX_GetUserExternalSession, WTSSBX_GetUserExternalSession method [Remote Desktop Services], WTSSBX_GetUserExternalSession method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_wtssbx_getuserexternalsession, tssbx/IWTSSBPlugin::WTSSBX_GetUserExternalSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tssbx.h
api_name:
 - IWTSSBPlugin.WTSSBX_GetUserExternalSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tssbx.h
: 
- IWTSSBPlugin.WTSSBX_GetUserExternalSession
: 
---

# IWTSSBPlugin::WTSSBX_GetUserExternalSession


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a> interface.]

Redirects an incoming connection to a computing resource, such as a virtual machine, a blade server, or even the user's own corporate desktop by providing a <a href="https://msdn.microsoft.com/805e606b-6f30-4f49-af04-b7f298c4fadf">WTSSBX_MACHINE_CONNECT_INFO</a> structure that contains information about the resource.


## -parameters




### -param UserName [in]

A pointer to a Unicode string  that contains the user name of the incoming connection.


### -param DomainName [in]

A pointer to a Unicode string  that contains the domain name of the incoming connection.


### -param ApplicationType [in]

A pointer to a Unicode string  that contains the program that Remote Desktop Services runs after the user session is created.


### -param RedirectorInternalIP [in]

A pointer to the internal IP address of the RD Session Host server that first accepted the connection.


### -param pSessionId

TBD


### -param pMachineConnectInfo [out]

A pointer to a <a href="https://msdn.microsoft.com/805e606b-6f30-4f49-af04-b7f298c4fadf">WTSSBX_MACHINE_CONNECT_INFO</a> structure that contains information about the computer to which the plug-in  is directing the incoming connection.


#### - pSessionID [out]

A pointer to the session ID of the session to which the plug-in is redirecting the incoming connection.


## -returns



Returns <b>S_OK</b> if successful.




## -remarks



Terminal Services Session Broker (TS Session Broker) calls this method so that the plug-in can redirect an incoming connection to a computer that is not joined to a farm in TS Session Broker.

Your implementation of <b>WTSSBX_GetUserExternalSession</b> should return <b>E_NOTIMPL</b> if it does not support redirection to computers that are not joined to farms in TS Session Broker.




## -see-also




<a href="https://msdn.microsoft.com/db3d3ee7-9e53-4bac-9711-4e85f1016db9">ITsSbPlugin</a>



<a href="https://msdn.microsoft.com/f6959b8c-a8a8-438b-8b6d-31bf0e782bac">IWTSSBPlugin</a>
 

 

