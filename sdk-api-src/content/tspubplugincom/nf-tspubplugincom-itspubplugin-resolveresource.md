---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

