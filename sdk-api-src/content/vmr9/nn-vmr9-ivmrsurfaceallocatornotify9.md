---
UID: NN:vmr9.IVMRSurfaceAllocatorNotify9
title: IVMRSurfaceAllocatorNotify9 (vmr9.h)
author: windows-sdk-content
description: The IVMRSurfaceAllocatorNotify9 interface is implemented by the Video Mixing Renderer Filter 9 (VMR-9).
old-location: dshow\ivmrsurfaceallocatornotify9.htm
tech.root: DirectShow
ms.assetid: f275b835-e5b3-46f4-8b26-a4b0e2554c7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocatorNotify9, IVMRSurfaceAllocatorNotify9 interface [DirectShow], IVMRSurfaceAllocatorNotify9 interface [DirectShow],described, IVMRSurfaceAllocatorNotify9Interface, dshow.ivmrsurfaceallocatornotify9, vmr9/IVMRSurfaceAllocatorNotify9
ms.topic: interface
f1_keywords: 
 - "vmr9/IVMRSurfaceAllocatorNotify9"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRSurfaceAllocatorNotify9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurfaceAllocatorNotify9 interface


## -description



The <b>IVMRSurfaceAllocatorNotify9</b> interface is implemented by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). Applications use this interface to set a custom allocator-presenter and the allocator-presenter uses this interface to inform the VMR of changes to the system environment that affect the Direct3D surfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocatorNotify9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocatorNotify9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRSurfaceAllocatorNotify9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator">AdviseSurfaceAllocator</a>
</td>
<td align="left" width="63%">
Called by an application to instruct the VMR to use a custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper">AllocateSurfaceHelper</a>
</td>
<td align="left" width="63%">
Allocates a Direct3D surface based on specified parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice">ChangeD3DDevice</a>
</td>
<td align="left" width="63%">
Notifies the VMR that the Direct3D playback device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-notifyevent">NotifyEvent</a>
</td>
<td align="left" width="63%">
Called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice">SetD3DDevice</a>
</td>
<td align="left" width="63%">
Sets the initial Direct3D device and monitor to be used for video playback.

</td>
</tr>
</table> 


## -remarks



The VMR-9 supports this interface in renderless mode only. Otherwise, <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> returns <b>E_NOINTERFACE</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/vmr-modes-of-operation">VMR Modes of Operation</a>.

Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a>
 

 

