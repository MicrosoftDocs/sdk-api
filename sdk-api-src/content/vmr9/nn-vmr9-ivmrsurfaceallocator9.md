---
UID: NN:vmr9.IVMRSurfaceAllocator9
title: IVMRSurfaceAllocator9
author: windows-sdk-content
description: The IVMRSurfaceAllocator9 interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 9 (VMR-9).
old-location: dshow\ivmrsurfaceallocator9.htm
old-project: DirectShow
ms.assetid: dd187168-19c7-414c-a764-f180d1d310f2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVMRSurfaceAllocator9, IVMRSurfaceAllocator9 interface [DirectShow], IVMRSurfaceAllocator9 interface [DirectShow],described, IVMRSurfaceAllocator9Interface, dshow.ivmrsurfaceallocator9, vmr9/IVMRSurfaceAllocator9
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
 - IVMRSurfaceAllocator9
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVMRSurfaceAllocator9 interface


## -description



The <b>IVMRSurfaceAllocator9</b> interface is implemented by the default allocator-presenter for the <a href="https://msdn.microsoft.com/3885cca2-74b1-4066-8ecb-84c9841f9e66">Video Mixing Renderer Filter 9</a> (VMR-9). It must also be implemented by any plug-in allocator-presenter object that an application provides to the VMR-9. The VMR-9 uses the methods on this interface to allocate, prepare and free Direct3D surfaces. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocator9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVMRSurfaceAllocator9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVMRSurfaceAllocator9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c367444-50bf-4fbe-b2d9-ed32275576e9">AdviseNotify</a>
</td>
<td align="left" width="63%">
Provides the allocator-presenter with the VMR-9 filter's interface for notification callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b14c7744-b5e5-484e-b5f3-99c4185a4e7c">GetSurface</a>
</td>
<td align="left" width="63%">
Retrieves a Direct3D surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44c22dc0-98a9-4a6e-a488-1d70dfff6acd">InitializeDevice</a>
</td>
<td align="left" width="63%">
Called by the VMR-9 when it needs the allocator-presenter to allocate surfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5006265d-6f2b-433b-b3ce-a7074d6eb159">TerminateDevice</a>
</td>
<td align="left" width="63%">
Releases the Direct3D device.

</td>
</tr>
</table> 


## -remarks



Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://msdn.microsoft.com/61bb6b0d-25b5-481b-a241-74c6e421f109">Supplying a Custom Allocator-Presenter for VMR-9</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

