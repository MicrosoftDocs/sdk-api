---
UID: NN:vmr9.IVMRSurfaceAllocatorNotify9
title: IVMRSurfaceAllocatorNotify9
author: windows-driver-content
description: The IVMRSurfaceAllocatorNotify9 interface is implemented by the Video Mixing Renderer Filter 9 (VMR-9).
old-location: dshow\ivmrsurfaceallocatornotify9.htm
old-project: DirectShow
ms.assetid: f275b835-e5b3-46f4-8b26-a4b0e2554c7c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IVMRSurfaceAllocatorNotify9, IVMRSurfaceAllocatorNotify9 interface [DirectShow], IVMRSurfaceAllocatorNotify9 interface [DirectShow], described, IVMRSurfaceAllocatorNotify9Interface, dshow.ivmrsurfaceallocatornotify9, vmr9/IVMRSurfaceAllocatorNotify9
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: VMR9DeinterlaceTech
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IVMRSurfaceAllocatorNotify9
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRSurfaceAllocatorNotify9 interface


## -description



The <b>IVMRSurfaceAllocatorNotify9</b> interface is implemented by the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9). Applications use this interface to set a custom allocator-presenter and the allocator-presenter uses this interface to inform the VMR of changes to the system environment that affect the Direct3D surfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocatorNotify9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRSurfaceAllocatorNotify9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/99f9c549-e4b1-480b-97a4-7a29c9cdb649">AdviseSurfaceAllocator</a>
</td>
<td align="left" width="63%">
Called by an application to instruct the VMR to use a custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b69db9e9-6ab0-40ad-b929-30613c0b9e4b">AllocateSurfaceHelper</a>
</td>
<td align="left" width="63%">
Allocates a Direct3D surface based on specified parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42199bdf-0cee-4dd0-98bc-66a8334b743b">ChangeD3DDevice</a>
</td>
<td align="left" width="63%">
Notifies the VMR that the Direct3D playback device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04c92e0f-9f6e-484c-96cd-3567c09a2ff6">NotifyEvent</a>
</td>
<td align="left" width="63%">
Called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f13fd7f4-03b3-4e10-9fe8-b81470b37253">SetD3DDevice</a>
</td>
<td align="left" width="63%">
Sets the initial Direct3D device and monitor to be used for video playback.

</td>
</tr>
</table> 


## -remarks



The VMR-9 supports this interface in renderless mode only. Otherwise, <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> returns <b>E_NOINTERFACE</b>. For more information, see <a href="https://msdn.microsoft.com/98244af1-5934-4d1c-b9c3-7a414b065fe7">VMR Modes of Operation</a>.


        Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>



<a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a>
 

 

