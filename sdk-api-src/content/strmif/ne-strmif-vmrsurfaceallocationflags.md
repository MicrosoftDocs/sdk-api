---
UID: NE:strmif.VMRSurfaceAllocationFlags
title: VMRSurfaceAllocationFlags (strmif.h)
description: The VMRSurfaceAllocationFlags enumeration is used with the IVMRSurfaceAllocator::AllocateSurface method to specify surface creation parameters.
helpviewer_keywords: ["AMAP_3D_TARGET","AMAP_ALLOW_SYSMEM","AMAP_DIRECTED_FLIP","AMAP_DXVA_TARGET","AMAP_FORCE_SYSMEM","AMAP_PIXELFORMAT_VALID","VMRSurfaceAllocationFlags","VMRSurfaceAllocationFlags enumeration [DirectShow]","VMR_ALLOCATE_SURFACE_FLAGSEnumeration","dshow.vmrsurfaceallocationflags","strmif/AMAP_3D_TARGET","strmif/AMAP_ALLOW_SYSMEM","strmif/AMAP_DIRECTED_FLIP","strmif/AMAP_DXVA_TARGET","strmif/AMAP_FORCE_SYSMEM","strmif/AMAP_PIXELFORMAT_VALID","strmif/VMRSurfaceAllocationFlags"]
old-location: dshow\vmrsurfaceallocationflags.htm
tech.root: dshow
ms.assetid: 1f75b357-0ce0-4efe-b1a8-39200e6b3d1a
ms.date: 12/05/2018
ms.keywords: AMAP_3D_TARGET, AMAP_ALLOW_SYSMEM, AMAP_DIRECTED_FLIP, AMAP_DXVA_TARGET, AMAP_FORCE_SYSMEM, AMAP_PIXELFORMAT_VALID, VMRSurfaceAllocationFlags, VMRSurfaceAllocationFlags enumeration [DirectShow], VMR_ALLOCATE_SURFACE_FLAGSEnumeration, dshow.vmrsurfaceallocationflags, strmif/AMAP_3D_TARGET, strmif/AMAP_ALLOW_SYSMEM, strmif/AMAP_DIRECTED_FLIP, strmif/AMAP_DXVA_TARGET, strmif/AMAP_FORCE_SYSMEM, strmif/AMAP_PIXELFORMAT_VALID, strmif/VMRSurfaceAllocationFlags
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
targetos: Windows
req.typenames: VMRSurfaceAllocationFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VMRSurfaceAllocationFlags
 - strmif/VMRSurfaceAllocationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRSurfaceAllocationFlags
---

# VMRSurfaceAllocationFlags enumeration


## -description

The <b>VMRSurfaceAllocationFlags</b> enumeration is used with the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-allocatesurface">IVMRSurfaceAllocator::AllocateSurface</a> method to specify surface creation parameters.

## -enum-fields

### -field AMAP_PIXELFORMAT_VALID:0x1

Indicates that the <b>lpPxFmt</b> field contains valid data that should be used to create the DirectDraw surface.

### -field AMAP_3D_TARGET:0x2

Indicates that the DirectDraw surface created should also be a Direct3D render target that is created with the <b>DDSCAPS_3DDEVICE</b> flag set.

### -field AMAP_ALLOW_SYSMEM:0x4

Indicates that if you can't allocate the DirectDraw surface in video memory you will try to allocate a system memory DirectDraw surface. (Note you should never allocate an AGP memory surface.)

### -field AMAP_FORCE_SYSMEM:0x8

Force the surface to be created in system memory. Specify this if you will use GDI to process the image before it is rendered. The surface must match the current monitor display format (pixel depth).

### -field AMAP_DIRECTED_FLIP:0x10

Means that when Flip is called you should Flip to the specified DirectDraw Surface passed as a parameter to the <a href="/windows/desktop/api/strmif/nf-strmif-ivmrimagepresenter-presentimage">PresentImage</a> method in the <a href="/windows/desktop/api/strmif/nn-strmif-ivmrimagepresenter">IVMRImagePresenter</a> interface. Correct support for this flag is crucial in order to keep DXVA buffers seen by a video decoder in sync with the DXVA buffers seen by the graphics driver.

### -field AMAP_DXVA_TARGET:0x20

Indicates that this surface will be used as a DXVA target.

## -remarks

AMAP_3D_TARGET cannot be combined with AMAP_FORCE_SYSMEM or AMAP_ALLOW_SYSMEM because 3D surfaces cannot be created in system memory.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrsurfaceallocator-allocatesurface">IVMRSurfaceAllocator::AllocateSurface</a>
