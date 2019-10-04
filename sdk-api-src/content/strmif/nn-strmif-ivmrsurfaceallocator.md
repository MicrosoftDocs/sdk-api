---
UID: NN:strmif.IVMRSurfaceAllocator
title: IVMRSurfaceAllocator (strmif.h)
author: windows-sdk-content
description: The IVMRSurfaceAllocator interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrsurfaceallocator.htm
tech.root: DirectShow
ms.assetid: bbcbe152-80fd-469b-a79b-c8db6f97da22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocator, IVMRSurfaceAllocator interface [DirectShow], IVMRSurfaceAllocator interface [DirectShow],described, IVMRSurfaceAllocatorInterface, dshow.ivmrsurfaceallocator, strmif/IVMRSurfaceAllocator
ms.topic: interface
f1_keywords: 
 - "strmif/IVMRSurfaceAllocator"
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
 - IVMRSurfaceAllocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurfaceAllocator interface


## -description



The <code>IVMRSurfaceAllocator</code> interface is implemented by the default allocator-presenter for the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in allocator-presenter that an application provides to the VMR-7. The VMR-7 uses the methods on this interface to allocate, prepare and free DirectDraw surfaces. Applications do not use this interface.

For the VMR-9, use the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRSurfaceAllocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-advisenotify">AdviseNotify</a>
</td>
<td align="left" width="63%">
Called by the VMR to provide the allocator-presenter with an interface pointer for notification callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-allocatesurface">AllocateSurface</a>
</td>
<td align="left" width="63%">
Allocates a DirectDraw surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-freesurface">FreeSurface</a>
</td>
<td align="left" width="63%">
Frees the allocated DirectDraw surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-preparesurface">PrepareSurface</a>
</td>
<td align="left" width="63%">
Prepares the DirectDraw surface to have the next video frame decoded into it.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

