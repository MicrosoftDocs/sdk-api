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

# IMFVideoSampleAllocatorCallback::SetCallback


## -description


Sets the callback object that receives notification whenever a video sample is returned to the allocator.


## -parameters




### -param pNotify [in]

A pointer to the <a href="https://msdn.microsoft.com/909c2a68-81dd-4816-b34f-71a67b620faf">IMFVideoSampleAllocatorNotify</a> interface that receives notification, or <b>NULL</b> to remove the callback.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get a video sample from the allocator, call the <a href="https://msdn.microsoft.com/e5347cef-edbd-4f6a-88c9-042e53515a32">IMFVideoSampleAllocator::AllocateSample</a> method. When the sample is released, it returns to the pool of available samples. When this happens, the allocator invokes the <a href="https://msdn.microsoft.com/0467ebbe-b00d-41c1-8f50-77ca09337b15">IMFVideoSampleAllocatorNotify::NotifyRelease</a> callback.

The allocator holds at most one callback pointer. Calling this method again replaces the previous callback pointer.




## -see-also




<a href="https://msdn.microsoft.com/7dbf8b3a-24b3-41d9-bb1e-9c57b88a77ac">IMFVideoSampleAllocatorCallback</a>
 

 

