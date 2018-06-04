---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

