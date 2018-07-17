---
UID: NN:strmif.IVMRSurfaceAllocator
title: IVMRSurfaceAllocator
author: windows-sdk-content
description: The IVMRSurfaceAllocator interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 7 (VMR-7).
old-location: dshow\ivmrsurfaceallocator.htm
old-project: DirectShow
ms.assetid: bbcbe152-80fd-469b-a79b-c8db6f97da22
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IVMRSurfaceAllocator, IVMRSurfaceAllocator interface [DirectShow], IVMRSurfaceAllocator interface [DirectShow],described, IVMRSurfaceAllocatorInterface, dshow.ivmrsurfaceallocator, strmif/IVMRSurfaceAllocator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IVMRSurfaceAllocator
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IVMRSurfaceAllocator interface


## -description



The <code>IVMRSurfaceAllocator</code> interface is implemented by the default allocator-presenter for the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in allocator-presenter that an application provides to the VMR-7. The VMR-7 uses the methods on this interface to allocate, prepare and free DirectDraw surfaces. Applications do not use this interface.

For the VMR-9, use the <a href="https://msdn.microsoft.com/dd187168-19c7-414c-a764-f180d1d310f2">IVMRSurfaceAllocator9</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRSurfaceAllocator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d4d9998f-e7d6-4c06-8a37-2e9c8e29106b">AdviseNotify</a>
</td>
<td align="left" width="63%">
Called by the VMR to provide the allocator-presenter with an interface pointer for notification callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6783df91-c92f-45d0-b299-16cdbc4bb630">AllocateSurface</a>
</td>
<td align="left" width="63%">
Allocates a DirectDraw surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b00d32c-832f-439f-8da5-7e77f90e1510">FreeSurface</a>
</td>
<td align="left" width="63%">
Frees the allocated DirectDraw surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5978bd6e-1aee-4e5e-9d28-f60e20b5b3e7">PrepareSurface</a>
</td>
<td align="left" width="63%">
Prepares the DirectDraw surface to have the next video frame decoded into it.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

