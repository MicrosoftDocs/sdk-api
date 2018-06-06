---
UID: NF:vmr9.IVMRSurfaceAllocatorNotify9.NotifyEvent
title: IVMRSurfaceAllocatorNotify9::NotifyEvent
author: windows-sdk-content
description: The NotifyEvent method is called by the allocator-presenter to inform the VMR of any significant DirectShow events that it (the allocator presenter) generates during the allocation or presentation processes.
old-location: dshow\ivmrsurfaceallocatornotify9_notifyevent.htm
old-project: DirectShow
ms.assetid: 04c92e0f-9f6e-484c-96cd-3567c09a2ff6
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVMRSurfaceAllocatorNotify9 interface [DirectShow],NotifyEvent method, IVMRSurfaceAllocatorNotify9.NotifyEvent, IVMRSurfaceAllocatorNotify9::NotifyEvent, IVMRSurfaceAllocatorNotify9NotifyEvent, NotifyEvent, NotifyEvent method [DirectShow], NotifyEvent method [DirectShow],IVMRSurfaceAllocatorNotify9 interface, dshow.ivmrsurfaceallocatornotify9_notifyevent, vmr9/IVMRSurfaceAllocatorNotify9::NotifyEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vmr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: VMR9DeinterlaceTech
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRSurfaceAllocatorNotify9.NotifyEvent
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRSurfaceAllocatorNotify9::NotifyEvent


## -description



The <code>NotifyEvent</code> method is called by the allocator-presenter to inform the VMR of any significant DirectShow events that it (the allocator presenter) generates during the allocation or presentation processes.




## -parameters




### -param EventCode [in]

Specifies the DirectShow event code.


### -param Param1 [in]

Specifies the first event parameter. The meaning depends on the event code. See <a href="https://msdn.microsoft.com/339ffcd9-7724-4c92-b241-afbed81d9380">Event Notification Codes</a>.


### -param Param2 [in]

Specifies the second event parameter. The meaning depends on the event code.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



The VMR provides the allocator-presenter with a pointer to this interface in a call to <a href="https://msdn.microsoft.com/2c367444-50bf-4fbe-b2d9-ed32275576e9">IVMRSurfaceAllocator9::AdviseNotify</a>. When the allocator-presenter calls this method and specifies some regular DirectShow event, such as EC_ERRORABORT or EC_VMR_RENDERDEVICE_SET, the VMR will pass the event to the filter graph manager.

Include DShow.h and D3d9.h before Vmr9.h.




## -see-also




<a href="https://msdn.microsoft.com/f275b835-e5b3-46f4-8b26-a4b0e2554c7c">IVMRSurfaceAllocatorNotify9 Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

