---
UID: NN:vmr9.IVMRSurfaceAllocatorEx9
title: IVMRSurfaceAllocatorEx9
author: windows-sdk-content
description: The IVMRSurfaceAllocatorEx9 interface provides a way for custom allocator-presenters to control where the Video Mixing Renderer Filter 9 (VMR-9) draws the composited image.
old-location: dshow\ivmrsurfaceallocatorex9.htm
old-project: DirectShow
ms.assetid: 4c43867f-6c4b-4ed7-af83-0133c997efcb
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IVMRSurfaceAllocatorEx9, IVMRSurfaceAllocatorEx9 interface [DirectShow], IVMRSurfaceAllocatorEx9 interface [DirectShow],described, IVMRSurfaceAllocatorEx9Interface, dshow.ivmrsurfaceallocatorex9, vmr9/IVMRSurfaceAllocatorEx9
ms.prod: windows
ms.technology: windows-sdk
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
 - IVMRSurfaceAllocatorEx9
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRSurfaceAllocatorEx9 interface


## -description



The <b>IVMRSurfaceAllocatorEx9</b> interface provides a way for custom allocator-presenters to control where the Video Mixing Renderer Filter 9 (VMR-9) draws the composited image.



To use this interface, implement it on your allocator-presenter. At the start of each frame, the VMR-9 calls <b>QueryInterface</b> on the allocator-presenter for the <b>IVMRSurfaceAllocatorEx9</b> interface. If the allocator-presenter returns the interface, the VMR-9 calls the <a href="https://msdn.microsoft.com/828f1ea6-4093-4a33-bc41-0f6fff752bcf">IVMRSurfaceAllocatorEx9::GetSurfaceEx</a> method instead of the usual <a href="https://msdn.microsoft.com/2fba7818-6395-47d3-98b3-347f1d4a7c6f">IVMRSurfaceAllocator9::GetSurface</a> method. This enables your allocator-presenter to specify the rectangle within the returned <b>IDirect3DSurface9</b> where the composed video image will be written. This feature enables all of the video image scaling operations to be performed in a single stage, and is available in both RGB and YUV mixing modes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocatorEx9</b> interface inherits from <a href="https://msdn.microsoft.com/dd187168-19c7-414c-a764-f180d1d310f2">IVMRSurfaceAllocator9</a>. <b>IVMRSurfaceAllocatorEx9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRSurfaceAllocatorEx9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/828f1ea6-4093-4a33-bc41-0f6fff752bcf">GetSurfaceEx</a>
</td>
<td align="left" width="63%">
Gets a Direct3D surface and a destination rectangle.

</td>
</tr>
</table> 


## -remarks




        Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://msdn.microsoft.com/dd187168-19c7-414c-a764-f180d1d310f2">IVMRSurfaceAllocator9</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

