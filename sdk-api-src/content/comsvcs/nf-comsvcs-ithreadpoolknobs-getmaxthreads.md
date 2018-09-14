---
UID: NF:comsvcs.IThreadPoolKnobs.GetMaxThreads
title: IThreadPoolKnobs::GetMaxThreads
author: windows-sdk-content
description: Retrieves the maximum number of threads that are allowed in the pool.
old-location: cos\ithreadpoolknobs_getmaxthreads.htm
tech.root: cossdk
ms.assetid: cf99a8f3-fe48-41f3-9162-8550981520a2
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetMaxThreads, GetMaxThreads method [COM+], GetMaxThreads method [COM+],IThreadPoolKnobs interface, IThreadPoolKnobs interface [COM+],GetMaxThreads method, IThreadPoolKnobs.GetMaxThreads, IThreadPoolKnobs::GetMaxThreads, _cos_IThreadPoolKnobs_GetMaxThreads, comsvcs/IThreadPoolKnobs::GetMaxThreads, cos.ithreadpoolknobs_getmaxthreads
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IThreadPoolKnobs.GetMaxThreads
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IThreadPoolKnobs::GetMaxThreads


## -description


Retrieves the maximum number of threads that are allowed in the pool.


## -parameters




### -param plcMaxThreads [out]

The maximum number of threads allowed in the pool. A zero value indicates that the pool can grow without limit.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/3d36e4ec-f4d4-407b-b671-4134886b7a2c">IThreadPoolKnobs</a>
 

 

