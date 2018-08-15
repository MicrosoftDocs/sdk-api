---
UID: NN:strmif.IVMRSurfaceAllocatorNotify
title: IVMRSurfaceAllocatorNotify
author: windows-sdk-content
description: The IVMRSurfaceAllocatorNotify interface is implemented by the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrsurfaceallocatornotify.htm
old-project: DirectShow
ms.assetid: c590c4cb-43ba-41c2-ab1f-28f7aeee0c87
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IVMRSurfaceAllocatorNotify, IVMRSurfaceAllocatorNotify interface [DirectShow], IVMRSurfaceAllocatorNotify interface [DirectShow],described, IVMRSurfaceAllocatorNotifyInterface, dshow.ivmrsurfaceallocatornotify, strmif/IVMRSurfaceAllocatorNotify
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVMRSurfaceAllocatorNotify
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRSurfaceAllocatorNotify interface


## -description



The <code>IVMRSurfaceAllocatorNotify</code> interface is implemented by the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). Applications use this interface to set a custom allocator-presenter and the allocator-presenter uses this interface to inform the VMR-7 of changes to the system environment that affect the DirectDraw surfaces.

In order for an application to obtain this interface, the VMR must be in renderless mode.

For the VMR-9, use the <a href="https://msdn.microsoft.com/f275b835-e5b3-46f4-8b26-a4b0e2554c7c">IVMRSurfaceAllocatorNotify9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocatorNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRSurfaceAllocatorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRSurfaceAllocatorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdb0837c-1ee3-4dc9-b797-3d726c8ba3dc">AdviseSurfaceAllocator</a>
</td>
<td align="left" width="63%">
Called by an application to instruct the VMR to use a custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fc4a001-7522-45b0-9b55-510f3ee3eb6d">ChangeDDrawDevice</a>
</td>
<td align="left" width="63%">
Notifies the VMR that the DirectDraw playback device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/566a889b-e6dc-42e7-ba71-0b0a17f3ae8c">NotifyEvent</a>
</td>
<td align="left" width="63%">
Called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b62df5fb-6759-4869-a6b3-f78978e1f5e2">RestoreDDrawSurfaces</a>
</td>
<td align="left" width="63%">
Notifies the VMR that a DirectDraw surface "loss" has been detected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29d4b9df-a498-4aff-8e85-51ede64d69dc">SetBorderColor</a>
</td>
<td align="left" width="63%">
Specifies to the VMR which color to use in areas of the display rectangle which are not being used for video, for example when the video is letterboxed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e6bd77e-8b2d-4cd8-9bd3-40a3fe9373f3">SetDDrawDevice</a>
</td>
<td align="left" width="63%">
Sets the initial DirectDraw device and monitor to be used for video playback.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

