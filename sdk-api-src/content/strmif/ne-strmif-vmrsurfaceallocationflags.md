---
UID: NE:strmif.VMRSurfaceAllocationFlags
title: VMRSurfaceAllocationFlags
author: windows-sdk-content
description: The VMRSurfaceAllocationFlags enumeration is used with the IVMRSurfaceAllocator::AllocateSurface method to specify surface creation parameters.
old-location: dshow\vmrsurfaceallocationflags.htm
tech.root: DirectShow
ms.assetid: 1f75b357-0ce0-4efe-b1a8-39200e6b3d1a
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: AMAP_3D_TARGET, AMAP_ALLOW_SYSMEM, AMAP_DIRECTED_FLIP, AMAP_DXVA_TARGET, AMAP_FORCE_SYSMEM, AMAP_PIXELFORMAT_VALID, VMRSurfaceAllocationFlags, VMRSurfaceAllocationFlags enumeration [DirectShow], VMR_ALLOCATE_SURFACE_FLAGSEnumeration, dshow.vmrsurfaceallocationflags, strmif/AMAP_3D_TARGET, strmif/AMAP_ALLOW_SYSMEM, strmif/AMAP_DIRECTED_FLIP, strmif/AMAP_DXVA_TARGET, strmif/AMAP_FORCE_SYSMEM, strmif/AMAP_PIXELFORMAT_VALID, strmif/VMRSurfaceAllocationFlags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRSurfaceAllocationFlags
product: Windows
targetos: Windows
req.typenames: VMRSurfaceAllocationFlags
req.redist: 
---

# VMRSurfaceAllocationFlags enumeration


## -description



The <b>VMRSurfaceAllocationFlags</b> enumeration is used with the <a href="https://msdn.microsoft.com/6783df91-c92f-45d0-b299-16cdbc4bb630">IVMRSurfaceAllocator::AllocateSurface</a> method to specify surface creation parameters.




## -enum-fields




### -field AMAP_PIXELFORMAT_VALID

Indicates that the <b>lpPxFmt</b> field contains valid data that should be used to create the DirectDraw surface.
          


### -field AMAP_3D_TARGET

Indicates that the DirectDraw surface created should also be a Direct3D render target that is created with the <b>DDSCAPS_3DDEVICE</b> flag set.
          


### -field AMAP_ALLOW_SYSMEM

Indicates that if you can't allocate the DirectDraw surface in video memory you will try to allocate a system memory DirectDraw surface. (Note you should never allocate an AGP memory surface.)


### -field AMAP_FORCE_SYSMEM

Force the surface to be created in system memory. Specify this if you will use GDI to process the image before it is renderered. The surface must match the current monitor display format (pixel depth).


### -field AMAP_DIRECTED_FLIP

Means that when Flip is called you should Flip to the specified DirectDraw Surface passed as a parameter to the <a href="https://msdn.microsoft.com/df6bf45d-df92-4655-862c-704a12a62ff9">PresentImage</a> method in the <a href="https://msdn.microsoft.com/cb9b1e29-45c3-4208-8343-c2924505a9f3">IVMRImagePresenter</a> interface. Correct support for this flag is crucial in order to keep DXVA buffers seen by a video decoder in sync with the DXVA buffers seen by the graphics driver.


### -field AMAP_DXVA_TARGET

Indicates that this surface will be used as a DXVA target.


## -remarks



AMAP_3D_TARGET cannot be combined with AMAP_FORCE_SYSMEM or AMAP_ALLOW_SYSMEM because 3D surfaces cannot be created in system memory.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/6783df91-c92f-45d0-b299-16cdbc4bb630">IVMRSurfaceAllocator::AllocateSurface</a>
 

 

