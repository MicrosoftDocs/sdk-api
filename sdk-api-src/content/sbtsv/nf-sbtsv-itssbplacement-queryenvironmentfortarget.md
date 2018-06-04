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

# ITsSbPlacement::QueryEnvironmentForTarget


## -description


Determines whether the specified environment is ready to host 
the target that was returned by load balancing.


## -parameters




### -param pConnection [in]

A pointer to an <a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a> client connection object.


### -param pPlacementSink [in]

 A pointer to an <a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a> placement sink object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Your plug-in should use the <a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a> object to report the state of the environment to Remote Desktop Connection Broker (RD Connection Broker).

After RD Connection Broker receives a load-balancing result, it calls <b>QueryEnvironmentForTarget</b> 
to determine whether the environment is present and ready.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/d90501dd-ca15-463c-b204-b1f56103ebe7">ITsSbPlacement</a>



<a href="https://msdn.microsoft.com/7abc5454-141a-47bc-b9cd-341b41a093d2">ITsSbPlacementNotifySink</a>
 

 

