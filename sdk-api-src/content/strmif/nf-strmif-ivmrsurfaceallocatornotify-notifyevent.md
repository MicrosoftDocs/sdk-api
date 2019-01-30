---
UID: NF:strmif.IVMRSurfaceAllocatorNotify.NotifyEvent
title: IVMRSurfaceAllocatorNotify::NotifyEvent
author: windows-sdk-content
description: The NotifyEvent method is called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.
old-location: dshow\ivmrsurfaceallocatornotify_notifyevent.htm
tech.root: DirectShow
ms.assetid: 566a889b-e6dc-42e7-ba71-0b0a17f3ae8c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVMRSurfaceAllocatorNotify interface [DirectShow],NotifyEvent method, IVMRSurfaceAllocatorNotify.NotifyEvent, IVMRSurfaceAllocatorNotify::NotifyEvent, IVMRSurfaceAllocatorNotifyNotifyEvent, NotifyEvent, NotifyEvent method [DirectShow], NotifyEvent method [DirectShow],IVMRSurfaceAllocatorNotify interface, dshow.ivmrsurfaceallocatornotify_notifyevent, strmif/IVMRSurfaceAllocatorNotify::NotifyEvent
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRSurfaceAllocatorNotify.NotifyEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVMRSurfaceAllocatorNotify::NotifyEvent


## -description



The <code>NotifyEvent</code> method is called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.




## -parameters




### -param EventCode [in]

Specifies the event code.


### -param Param1 [in]

Specifies Param1 of the event code.


### -param Param2 [in]

Specifies Param2 of the event code.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



The VMR provides the allocator-presenter with a pointer to this interface in a call to <a href="https://msdn.microsoft.com/d4d9998f-e7d6-4c06-8a37-2e9c8e29106b">IVMRSurfaceAllocator::AdviseNotify</a>. When the allocator-presenter calls this method and specifies some regular DirectShow event, such as EC_ERRORABORT or EC_VMR_RENDERDEVICE_SET, the VMR will pass the event to the filter graph manager.




## -see-also




<a href="https://msdn.microsoft.com/c590c4cb-43ba-41c2-ab1f-28f7aeee0c87">IVMRSurfaceAllocatorNotify Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

