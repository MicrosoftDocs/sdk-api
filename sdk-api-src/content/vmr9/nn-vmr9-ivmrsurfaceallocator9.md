---
UID: NN:vmr9.IVMRSurfaceAllocator9
title: IVMRSurfaceAllocator9 (vmr9.h)
description: The IVMRSurfaceAllocator9 interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 9 (VMR-9).
helpviewer_keywords: ["IVMRSurfaceAllocator9","IVMRSurfaceAllocator9 interface [DirectShow]","IVMRSurfaceAllocator9 interface [DirectShow]","described","IVMRSurfaceAllocator9Interface","dshow.ivmrsurfaceallocator9","vmr9/IVMRSurfaceAllocator9"]
old-location: dshow\ivmrsurfaceallocator9.htm
tech.root: dshow
ms.assetid: dd187168-19c7-414c-a764-f180d1d310f2
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocator9, IVMRSurfaceAllocator9 interface [DirectShow], IVMRSurfaceAllocator9 interface [DirectShow],described, IVMRSurfaceAllocator9Interface, dshow.ivmrsurfaceallocator9, vmr9/IVMRSurfaceAllocator9
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
 - IVMRSurfaceAllocator9
 - vmr9/IVMRSurfaceAllocator9
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
 - IVMRSurfaceAllocator9
---

# IVMRSurfaceAllocator9 interface


## -description

The <b>IVMRSurfaceAllocator9</b> interface is implemented by the default allocator-presenter for the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9). It must also be implemented by any plug-in allocator-presenter object that an application provides to the VMR-9. The VMR-9 uses the methods on this interface to allocate, prepare and free Direct3D surfaces. Applications do not use this interface.

## -inheritance

The <b>IVMRSurfaceAllocator9</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocator9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

Include DShow.h and D3d9.h before Vmr9.h.

## -see-also

<a href="/windows/desktop/DirectShow/supplying-a-custom-allocator-presenter-for-vmr-9">Supplying a Custom Allocator-Presenter for VMR-9</a>



<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
