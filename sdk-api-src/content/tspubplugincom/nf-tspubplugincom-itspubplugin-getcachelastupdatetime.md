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

# ItsPubPlugin::GetCacheLastUpdateTime


## -description


Returns the time that the cache was last updated. The RemoteApp and Desktop Connection Management service calls this method to determine whether the data in the Remote Desktop Web Access (RD Web Access) cache should be refreshed. 


## -parameters




### -param lastUpdateTime [out]

A pointer to an  <b>unsigned long long</b> variable that receives the time that the cache was last updated.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The RemoteApp and Desktop Connection Management service calls this method to get the last time that the cache was refreshed. If your plug-in does not implement caching, return the current system time. This tells the service that it must call <a href="https://msdn.microsoft.com/c8f255fe-6f31-4cbb-a600-a27e977a84a0">GetResourceList</a> to get the current list of resources. We recommend implementing the plug-in with caching because caching reduces the number of calls the service must make to <b>GetResourceList</b>.




## -see-also




<a href="https://msdn.microsoft.com/37d33f27-a811-4c97-bc80-ff8a5b8fcb7c">ItsPubPlugin</a>
 

 

