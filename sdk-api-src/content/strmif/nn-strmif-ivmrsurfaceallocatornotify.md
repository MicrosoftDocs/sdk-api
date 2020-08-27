---
UID: NN:strmif.IVMRSurfaceAllocatorNotify
title: IVMRSurfaceAllocatorNotify (strmif.h)
description: The IVMRSurfaceAllocatorNotify interface is implemented by the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRSurfaceAllocatorNotify","IVMRSurfaceAllocatorNotify interface [DirectShow]","IVMRSurfaceAllocatorNotify interface [DirectShow]","described","IVMRSurfaceAllocatorNotifyInterface","dshow.ivmrsurfaceallocatornotify","strmif/IVMRSurfaceAllocatorNotify"]
old-location: dshow\ivmrsurfaceallocatornotify.htm
tech.root: dshow
ms.assetid: c590c4cb-43ba-41c2-ab1f-28f7aeee0c87
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocatorNotify, IVMRSurfaceAllocatorNotify interface [DirectShow], IVMRSurfaceAllocatorNotify interface [DirectShow],described, IVMRSurfaceAllocatorNotifyInterface, dshow.ivmrsurfaceallocatornotify, strmif/IVMRSurfaceAllocatorNotify
f1_keywords:
- strmif/IVMRSurfaceAllocatorNotify
dev_langs:
- c++
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
- IVMRSurfaceAllocatorNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurfaceAllocatorNotify interface


## -description



The <code>IVMRSurfaceAllocatorNotify</code> interface is implemented by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). Applications use this interface to set a custom allocator-presenter and the allocator-presenter uses this interface to inform the VMR-7 of changes to the system environment that affect the DirectDraw surfaces.

In order for an application to obtain this interface, the VMR must be in renderless mode.

For the VMR-9, use the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocatornotify9">IVMRSurfaceAllocatorNotify9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocatorNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocatorNotify</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator">AdviseSurfaceAllocator</a>
</td>
<td align="left" width="63%">
Called by an application to instruct the VMR to use a custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocatornotify-changeddrawdevice">ChangeDDrawDevice</a>
</td>
<td align="left" width="63%">
Notifies the VMR that the DirectDraw playback device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent">NotifyEvent</a>
</td>
<td align="left" width="63%">
Called by the allocator-presenter to inform the VMR of any significant DirectShow events during the allocation or presentation processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocatornotify-restoreddrawsurfaces">RestoreDDrawSurfaces</a>
</td>
<td align="left" width="63%">
Notifies the VMR that a DirectDraw surface "loss" has been detected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocatornotify-setbordercolor">SetBorderColor</a>
</td>
<td align="left" width="63%">
Specifies to the VMR which color to use in areas of the display rectangle which are not being used for video, for example when the video is letterboxed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocatornotify-setddrawdevice">SetDDrawDevice</a>
</td>
<td align="left" width="63%">
Sets the initial DirectDraw device and monitor to be used for video playback.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

