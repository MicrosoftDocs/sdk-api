---
UID: NF:vmr9.IVMRSurfaceAllocatorNotify9.NotifyEvent
title: IVMRSurfaceAllocatorNotify9::NotifyEvent (vmr9.h)
description: The NotifyEvent method is called by the allocator-presenter to inform the VMR of any significant DirectShow events that it (the allocator presenter) generates during the allocation or presentation processes.
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify9 interface [DirectShow]","NotifyEvent method","IVMRSurfaceAllocatorNotify9.NotifyEvent","IVMRSurfaceAllocatorNotify9::NotifyEvent","IVMRSurfaceAllocatorNotify9NotifyEvent","NotifyEvent","NotifyEvent method [DirectShow]","NotifyEvent method [DirectShow]","IVMRSurfaceAllocatorNotify9 interface","dshow.ivmrsurfaceallocatornotify9_notifyevent","vmr9/IVMRSurfaceAllocatorNotify9::NotifyEvent"]
old-location: dshow\ivmrsurfaceallocatornotify9_notifyevent.htm
tech.root: dshow
ms.assetid: 04c92e0f-9f6e-484c-96cd-3567c09a2ff6
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocatorNotify9 interface [DirectShow],NotifyEvent method, IVMRSurfaceAllocatorNotify9.NotifyEvent, IVMRSurfaceAllocatorNotify9::NotifyEvent, IVMRSurfaceAllocatorNotify9NotifyEvent, NotifyEvent, NotifyEvent method [DirectShow], NotifyEvent method [DirectShow],IVMRSurfaceAllocatorNotify9 interface, dshow.ivmrsurfaceallocatornotify9_notifyevent, vmr9/IVMRSurfaceAllocatorNotify9::NotifyEvent
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRSurfaceAllocatorNotify9::NotifyEvent
 - vmr9/IVMRSurfaceAllocatorNotify9::NotifyEvent
dev_langs:
 - c++
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
---

# IVMRSurfaceAllocatorNotify9::NotifyEvent


## -description

The <code>NotifyEvent</code> method is called by the allocator-presenter to inform the VMR of any significant DirectShow events that it (the allocator presenter) generates during the allocation or presentation processes.

## -parameters

### -param EventCode [in]

Specifies the DirectShow event code.

### -param Param1 [in]

Specifies the first event parameter. The meaning depends on the event code. See <a href="/windows/desktop/DirectShow/event-notification-codes">Event Notification Codes</a>.

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

The VMR provides the allocator-presenter with a pointer to this interface in a call to <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify">IVMRSurfaceAllocator9::AdviseNotify</a>. When the allocator-presenter calls this method and specifies some regular DirectShow event, such as EC_ERRORABORT or EC_VMR_RENDERDEVICE_SET, the VMR will pass the event to the filter graph manager.

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9 Interface</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>