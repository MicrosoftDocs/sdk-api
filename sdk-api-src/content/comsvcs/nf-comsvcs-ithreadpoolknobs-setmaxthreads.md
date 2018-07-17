---
UID: NF:comsvcs.IThreadPoolKnobs.SetMaxThreads
title: IThreadPoolKnobs::SetMaxThreads
author: windows-sdk-content
description: Sets the maximum number of threads to be allowed in the pool.
old-location: cos\ithreadpoolknobs_setmaxthreads.htm
old-project: cossdk
ms.assetid: abca2ec3-4dcd-4770-a500-1d46b87b4cda
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IThreadPoolKnobs interface [COM+],SetMaxThreads method, IThreadPoolKnobs.SetMaxThreads, IThreadPoolKnobs::SetMaxThreads, SetMaxThreads, SetMaxThreads method [COM+], SetMaxThreads method [COM+],IThreadPoolKnobs interface, _cos_IThreadPoolKnobs_SetMaxThreads, comsvcs/IThreadPoolKnobs::SetMaxThreads, cos.ithreadpoolknobs_setmaxthreads
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IThreadPoolKnobs.SetMaxThreads
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IThreadPoolKnobs::SetMaxThreads


## -description


Sets the maximum number of threads to be allowed in the pool.


## -parameters




### -param lcMaxThreads [in]

The maximum number of threads allowed in the pool. A zero value indicates that the pool can grow without limit.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/3d36e4ec-f4d4-407b-b671-4134886b7a2c">IThreadPoolKnobs</a>
 

 

