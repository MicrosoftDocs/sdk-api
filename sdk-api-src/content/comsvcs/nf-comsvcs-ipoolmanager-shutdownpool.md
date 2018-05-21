---
UID: NF:comsvcs.IPoolManager.ShutdownPool
title: IPoolManager::ShutdownPool
author: windows-driver-content
description: Shuts down the object pool.
old-location: cos\ipoolmanager_shutdownpool.htm
old-project: cossdk
ms.assetid: c374b0a4-d984-4fa6-80a7-8bc4d0aff284
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IPoolManager interface [COM+],ShutdownPool method, IPoolManager.ShutdownPool, IPoolManager::ShutdownPool, ShutdownPool, ShutdownPool method [COM+], ShutdownPool method [COM+],IPoolManager interface, _cos_IPoolManager_ShutdownPool, comsvcs/IPoolManager::ShutdownPool, cos.ipoolmanager_shutdownpool
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IPoolManager.ShutdownPool
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IPoolManager::ShutdownPool


## -description


Shuts down the object pool.


## -parameters




### -param CLSIDOrProgID [in]

A string containing the CLSID or ProgID of the pool to be shut down.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/7811ad0c-e7b6-423b-8c52-ab8b1b97d6f4">IPoolManager</a>
 

 

