---
UID: NF:comsvcs.IThreadPoolKnobs.GetDeleteDelay
title: IThreadPoolKnobs::GetDeleteDelay (comsvcs.h)
author: windows-sdk-content
description: Retrieves the number of milliseconds a pooled thread can idle before being destroyed.
old-location: cos\ithreadpoolknobs_getdeletedelay.htm
tech.root: cossdk
ms.assetid: 93404c39-b4f8-4247-a437-fd373b0b68fe
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDeleteDelay, GetDeleteDelay method [COM+], GetDeleteDelay method [COM+],IThreadPoolKnobs interface, IThreadPoolKnobs interface [COM+],GetDeleteDelay method, IThreadPoolKnobs.GetDeleteDelay, IThreadPoolKnobs::GetDeleteDelay, _cos_IThreadPoolKnobs_GetDeleteDelay, comsvcs/IThreadPoolKnobs::GetDeleteDelay, cos.ithreadpoolknobs_getdeletedelay
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
 - IThreadPoolKnobs.GetDeleteDelay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IThreadPoolKnobs::GetDeleteDelay


## -description


Retrieves the number of milliseconds a pooled thread can idle before being destroyed.


## -parameters




### -param pmsecDeleteDelay [out]

The number of milliseconds a pooled thread can idle before being destroyed. A zero value indicates that threads are never automatically deleted.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/3d36e4ec-f4d4-407b-b671-4134886b7a2c">IThreadPoolKnobs</a>
 

 

