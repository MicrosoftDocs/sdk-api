---
UID: NN:vmr9.IVMRSurfaceAllocator9
title: IVMRSurfaceAllocator9 (vmr9.h)

description: The IVMRSurfaceAllocator9 interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 9 (VMR-9).
old-location: dshow\ivmrsurfaceallocator9.htm
tech.root: DirectShow
ms.assetid: dd187168-19c7-414c-a764-f180d1d310f2

ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocator9, IVMRSurfaceAllocator9 interface [DirectShow], IVMRSurfaceAllocator9 interface [DirectShow],described, IVMRSurfaceAllocator9Interface, dshow.ivmrsurfaceallocator9, vmr9/IVMRSurfaceAllocator9
ms.topic: interface
f1_keywords: 
 - "vmr9/IVMRSurfaceAllocator9"
dev_langs:
 - c++
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
 - IVMRSurfaceAllocator9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurfaceAllocator9 interface


## -description



The <b>IVMRSurfaceAllocator9</b> interface is implemented by the default allocator-presenter for the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). It must also be implemented by any plug-in allocator-presenter object that an application provides to the VMR-9. The VMR-9 uses the methods on this interface to allocate, prepare and free Direct3D surfaces. Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVMRSurfaceAllocator9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocator9</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify">AdviseNotify</a>
</td>
<td align="left" width="63%">
Provides the allocator-presenter with the VMR-9 filter's interface for notification callbacks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface">GetSurface</a>
</td>
<td align="left" width="63%">
Retrieves a Direct3D surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice">InitializeDevice</a>
</td>
<td align="left" width="63%">
Called by the VMR-9 when it needs the allocator-presenter to allocate surfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice">TerminateDevice</a>
</td>
<td align="left" width="63%">
Releases the Direct3D device.

</td>
</tr>
</table> 


## -remarks



Include DShow.h and D3d9.h before Vmr9.h.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/supplying-a-custom-allocator-presenter-for-vmr-9">Supplying a Custom Allocator-Presenter for VMR-9</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

