---
UID: NN:strmif.IVMRSurfaceAllocator
title: IVMRSurfaceAllocator (strmif.h)
description: The IVMRSurfaceAllocator interface is implemented by the default allocator-presenter for the Video Mixing Renderer Filter 7 (VMR-7).
helpviewer_keywords: ["IVMRSurfaceAllocator","IVMRSurfaceAllocator interface [DirectShow]","IVMRSurfaceAllocator interface [DirectShow]","described","IVMRSurfaceAllocatorInterface","dshow.ivmrsurfaceallocator","strmif/IVMRSurfaceAllocator"]
old-location: dshow\ivmrsurfaceallocator.htm
tech.root: dshow
ms.assetid: bbcbe152-80fd-469b-a79b-c8db6f97da22
ms.date: 12/05/2018
ms.keywords: IVMRSurfaceAllocator, IVMRSurfaceAllocator interface [DirectShow], IVMRSurfaceAllocator interface [DirectShow],described, IVMRSurfaceAllocatorInterface, dshow.ivmrsurfaceallocator, strmif/IVMRSurfaceAllocator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVMRSurfaceAllocator
 - strmif/IVMRSurfaceAllocator
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
 - IVMRSurfaceAllocator
---

# IVMRSurfaceAllocator interface


## -description

The <code>IVMRSurfaceAllocator</code> interface is implemented by the default allocator-presenter for the <a href="/windows/desktop/DirectShow/video-mixing-renderer-filter-7">Video Mixing Renderer Filter 7</a> (VMR-7). It must also be implemented by any plug-in allocator-presenter that an application provides to the VMR-7. The VMR-7 uses the methods on this interface to allocate, prepare and free DirectDraw surfaces. Applications do not use this interface.

For the VMR-9, use the <a href="/previous-versions/windows/desktop/api/vmr9/nn-vmr9-ivmrsurfaceallocator9">IVMRSurfaceAllocator9</a> interface.

## -inheritance

The <b>IVMRSurfaceAllocator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVMRSurfaceAllocator</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
