---
UID: NF:tspubplugincom.ItsPubPlugin.ResolveResource
title: ItsPubPlugin::ResolveResource
author: windows-sdk-content
description: Provides information about how to connect to a user's assigned personal virtual desktop.
old-location: termserv\itspubplugin_resolveresource.htm
old-project: termserv
ms.assetid: 035b9d13-b64e-4e1c-8623-b4456f36c4ee
ms.author: windowssdkdev
ms.date: 07/10/2018
ms.keywords: ItsPubPlugin interface [Remote Desktop Services],ResolveResource method, ItsPubPlugin.ResolveResource, ItsPubPlugin::ResolveResource, ResolveResource, ResolveResource method [Remote Desktop Services], ResolveResource method [Remote Desktop Services],ItsPubPlugin interface, termserv.itspubplugin_resolveresource, tspubplugincom/ItsPubPlugin::ResolveResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tspubplugincom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Cpubplugin.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: pluginResource2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tspubplugincom.h
api_name:
 - ItsPubPlugin.ResolveResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ItsPubPlugin::ResolveResource


## -description


 Provides information about how to connect to a user's assigned personal virtual desktop. Implement this method if you want to provide a custom implementation of the personal virtual desktop functionality.

Otherwise, this method should return <b>E_NOTIMPL</b>. This method is called by the RemoteApp and Desktop Connection Management service when Remote Desktop Connection Broker (RD Connection Broker) is connecting a user to a personal virtual desktop. 


## -parameters




### -param resourceType [out]

A pointer to a <b>DWORD</b> variable to receive the type of resource. This can be one of the following values.



#### 1

The plug-in is for virtual desktop pools.



#### 2

The plug-in is for personal virtual desktops.


### -param resourceLocation [out]

The name of the resource plug-in.


### -param endPointName [out]

The name of the endpoint. For personal virtual desktops, specify the name of the desktop assigned to the user. For virtual desktop pools, specify the name of the pool.


### -param userID [in]

A pointer to a string that contains the user security identifier (SID).


### -param alias [in]

A pointer to a string that contains the alias of the user.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



RD Connection Broker only calls one plug-in when connecting a user to a resource. To receive calls, you must register your plug-in before starting RD Connection Broker, or you must add a "LoadBalanceInfo" setting to the .rdp file that the client uses to connect. For example, if your plug-in is for personal virtual desktops and is called "plugin1", you would add the following line to the .rdp file: "LoadBalanceInfo:s:tsv://vmresource1.2.plugin1"




## -see-also




<a href="https://msdn.microsoft.com/37d33f27-a811-4c97-bc80-ff8a5b8fcb7c">ItsPubPlugin</a>
 

 

