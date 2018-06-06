---
UID: NF:strmif.IVMRSurfaceAllocator.FreeSurface
title: IVMRSurfaceAllocator::FreeSurface
author: windows-sdk-content
description: The FreeSurface method frees the allocated DirectDraw surface.
old-location: dshow\ivmrsurfaceallocator_freesurface.htm
old-project: DirectShow
ms.assetid: 7b00d32c-832f-439f-8da5-7e77f90e1510
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: FreeSurface, FreeSurface method [DirectShow], FreeSurface method [DirectShow],IVMRSurfaceAllocator interface, IVMRSurfaceAllocator interface [DirectShow],FreeSurface method, IVMRSurfaceAllocator.FreeSurface, IVMRSurfaceAllocator::FreeSurface, IVMRSurfaceAllocatorFreeSurface, dshow.ivmrsurfaceallocator_freesurface, strmif/IVMRSurfaceAllocator::FreeSurface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IVMRSurfaceAllocator.FreeSurface
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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




<a href="https://msdn.microsoft.com/bbcbe152-80fd-469b-a79b-c8db6f97da22">IVMRSurfaceAllocator Interface</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

