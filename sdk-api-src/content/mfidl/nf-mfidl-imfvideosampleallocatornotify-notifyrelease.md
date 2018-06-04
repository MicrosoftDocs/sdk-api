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

# IMFVideoSampleAllocatorNotify::NotifyRelease


## -description


Called when a video sample is returned to the allocator.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get a video sample from the allocator, call the <a href="https://msdn.microsoft.com/e5347cef-edbd-4f6a-88c9-042e53515a32">IMFVideoSampleAllocator::AllocateSample</a> method. When the sample is released and then returned to the pool of available samples, the allocator invokes the <b>NotifyRelease</b> method. 




## -see-also




<a href="https://msdn.microsoft.com/909c2a68-81dd-4816-b34f-71a67b620faf">IMFVideoSampleAllocatorNotify</a>



<a href="https://msdn.microsoft.com/5B3EA486-A45F-4C7B-8E36-80C9C2FD64F2">IMFVideoSampleAllocatorNotifyEx</a>
 

 

