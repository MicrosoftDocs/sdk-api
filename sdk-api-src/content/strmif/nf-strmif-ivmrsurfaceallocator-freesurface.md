---
UID: NF:strmif.IVMRSurfaceAllocator.FreeSurface
title: IVMRSurfaceAllocator::FreeSurface (strmif.h)
description: The FreeSurface method frees the allocated DirectDraw surface.
helpviewer_keywords: ["FreeSurface","FreeSurface method [DirectShow]","FreeSurface method [DirectShow]","IVMRSurfaceAllocator interface","IVMRSurfaceAllocator interface [DirectShow]","FreeSurface method","IVMRSurfaceAllocator.FreeSurface","IVMRSurfaceAllocator::FreeSurface","IVMRSurfaceAllocatorFreeSurface","dshow.ivmrsurfaceallocator_freesurface","strmif/IVMRSurfaceAllocator::FreeSurface"]
old-location: dshow\ivmrsurfaceallocator_freesurface.htm
tech.root: dshow
ms.assetid: 7b00d32c-832f-439f-8da5-7e77f90e1510
ms.date: 12/05/2018
ms.keywords: FreeSurface, FreeSurface method [DirectShow], FreeSurface method [DirectShow],IVMRSurfaceAllocator interface, IVMRSurfaceAllocator interface [DirectShow],FreeSurface method, IVMRSurfaceAllocator.FreeSurface, IVMRSurfaceAllocator::FreeSurface, IVMRSurfaceAllocatorFreeSurface, dshow.ivmrsurfaceallocator_freesurface, strmif/IVMRSurfaceAllocator::FreeSurface
f1_keywords:
- strmif/IVMRSurfaceAllocator.FreeSurface
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
- IVMRSurfaceAllocator.FreeSurface
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVMRSurfaceAllocator::FreeSurface


## -description



The <code>FreeSurface</code> method frees the allocated DirectDraw surface.




## -parameters




### -param dwID [in]

An application-defined DWORD_PTR cookie that uniquely identifies this instance of the VMR for use in scenarios when one instance of the allocator-presenter is used with multiple VMR instances.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ivmrsurfaceallocator">IVMRSurfaceAllocator Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>
 

 

