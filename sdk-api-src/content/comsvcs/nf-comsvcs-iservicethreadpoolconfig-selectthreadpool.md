---
UID: NF:comsvcs.IServiceThreadPoolConfig.SelectThreadPool
title: IServiceThreadPoolConfig::SelectThreadPool
author: windows-sdk-content
description: Selects the thread pool in which the work submitted through the activity is to run.
old-location: cos\iservicethreadpoolconfig_selectthreadpool.htm
old-project: cossdk
ms.assetid: eba8b4fc-aee7-4ba5-8e0e-b74ce9d25a86
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IServiceThreadPoolConfig interface [COM+],SelectThreadPool method, IServiceThreadPoolConfig.SelectThreadPool, IServiceThreadPoolConfig::SelectThreadPool, SelectThreadPool, SelectThreadPool method [COM+], SelectThreadPool method [COM+],IServiceThreadPoolConfig interface, _cos_IServiceThreadPoolConfig_SelectThreadPool, comsvcs/IServiceThreadPoolConfig::SelectThreadPool, cos.iservicethreadpoolconfig_selectthreadpool
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServiceThreadPoolConfig.SelectThreadPool
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceThreadPoolConfig::SelectThreadPool


## -description


Selects the thread pool in which the work submitted through the activity is to run.


## -parameters




### -param threadPool [in]

A value from the <a href="https://msdn.microsoft.com/5acf5c6b-b015-448b-ad4c-e4361a97c31e">CSC_ThreadPool</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/89c04fef-c6a0-4d73-a25a-a70b4b0f0bcf">IServiceThreadPoolConfig</a>
 

 

