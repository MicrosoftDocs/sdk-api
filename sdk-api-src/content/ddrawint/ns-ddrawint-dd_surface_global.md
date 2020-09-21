---
UID: NS:ddrawint._DD_SURFACE_GLOBAL
title: DD_SURFACE_GLOBAL (ddrawint.h)
description: The DD_SURFACE_GLOBAL structure contains global surface-related data that can be shared between multiple surfaces.
helpviewer_keywords: ["*PDD_SURFACE_GLOBAL","DD_SURFACE_GLOBAL","DD_SURFACE_GLOBAL structure [Display Devices]","PDD_SURFACE_GLOBAL","PDD_SURFACE_GLOBAL structure pointer [Display Devices]","ddrawint/DD_SURFACE_GLOBAL","ddrawint/PDD_SURFACE_GLOBAL","ddstrcts_83ae0625-9b08-4380-bd3a-d8d67675a48b.xml","display.dd_surface_global"]
old-location: display\dd_surface_global.htm
tech.root: display
ms.assetid: 11e0a6b9-16b9-4fc3-8e17-776f56c12196
ms.date: 12/05/2018
ms.keywords: '*PDD_SURFACE_GLOBAL, DD_SURFACE_GLOBAL, DD_SURFACE_GLOBAL structure [Display Devices], PDD_SURFACE_GLOBAL, PDD_SURFACE_GLOBAL structure pointer [Display Devices], ddrawint/DD_SURFACE_GLOBAL, ddrawint/PDD_SURFACE_GLOBAL, ddstrcts_83ae0625-9b08-4380-bd3a-d8d67675a48b.xml, display.dd_surface_global'
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: '*PDD_SURFACE_GLOBAL, DD_SURFACE_GLOBAL'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_SURFACE_GLOBAL
 - ddrawint/_DD_SURFACE_GLOBAL
 - PDD_SURFACE_GLOBAL
 - ddrawint/PDD_SURFACE_GLOBAL
 - DD_SURFACE_GLOBAL
 - ddrawint/DD_SURFACE_GLOBAL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_SURFACE_GLOBAL
---

# DD_SURFACE_GLOBAL structure


## -description

The DD_SURFACE_GLOBAL structure contains global surface-related data that can be shared between multiple surfaces.

## -struct-fields

### -field dwBlockSizeY

Specifies the location in which the driver returns the height, in scan lines, of the offscreen memory block that Microsoft DirectDraw should allocate. The driver should set this value when it returns DDHAL_PLEASEALLOC_BLOCKSIZE in the <b>fpVidMem</b> member.

### -field lSlicePitch

Slice pitch for volume textures.

### -field lpVidMemHeap

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a> structure from which the heap display memory was allocated.

### -field dwBlockSizeX

Specifies the location in which the driver returns the size in bytes of the width of the offscreen memory block that DirectDraw should allocate. The driver should set this value when it returns DDHAL_PLEASEALLOC_BLOCKSIZE in the <b>fpVidMem</b> member.

### -field dwUserMemSize

Specifies the location in which the driver returns the size in bytes of the memory block that DirectDraw should allocate in user-mode system memory. The driver should set this value when it returns DDHAL_PLEASEALLOC_USERMEM in the <b>fpVidMem</b> member.

### -field fpVidMem

If the driver allocates the memory block, it should return the offset into display memory in this member. If the driver requests DirectDraw to do the memory allocation, it can instead return one of the following values in this member from its <a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a> routine:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDHAL_PLEASEALLOC_BLOCKSIZE

</td>
<td>
DirectDraw should allocate a memory block of size <b>dwBlockSizeX</b> and <b>dwBlockSizeY</b> in offscreen memory.

</td>
</tr>
<tr>
<td>
DDHAL_PLEASEALLOC_USERMEM

</td>
<td>
DirectDraw should allocate a memory block of size <b>dwUserMemSize</b> in user-mode memory.

</td>
</tr>
</table>

### -field lPitch

Specifies the pitch of the surface; that is, the distance in bytes to the start of the next line. This is also known as the stride of the surface.

### -field dwLinearSize

Specifies the linear size in bytes of a nonrectangular surface.

### -field yHint

Specifies the y-coordinate of the surface. This member is a 2D Cartesian coordinate specified in device space.

### -field xHint

Specifies the x-coordinate of the surface. This member is a 2D Cartesian coordinate specified in device space.

### -field wHeight

Specifies the height in pixels of the surface.

### -field wWidth

Specifies the width in pixels of the surface.

### -field dwReserved1

Reserved for use by the display driver.

### -field ddpfSurface

Points to the <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a> structure that describes the pixel format of the surface.

### -field fpHeapOffset

Points to the raw offset in the source heap.

### -field hCreatorProcess

Reserved for system use and should be ignored by the driver.

## -remarks

A <a href="/windows-hardware/drivers/display/direct3d-vertex-buffers">vertex buffer</a>, which is created by <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a>, holds a list of vertices used by the <a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a> callback for rendering primitives. Microsoft Windows represents vertex buffers as DirectDraw surfaces, thereby establishing a connection between vertex buffers and the DD_SURFACE_GLOBAL structure.

When a DirectX driver is working with a vertex buffer, it is important for it to be able to correctly determine the size of this buffer. DirectDraw passes the linear buffer size to the driver in the <b>lPitch</b> member of this structure. On Windows 2000 and later versions, but not on Windows 98/Me, the <b>wWidth</b> member of this structure is set to the same value. Note that both structure members should be considered to be read-only. The value that DirectDraw places in these members represents the minimum vertex buffer size. Should the need for a larger buffer arise (such as for optimization), a driver writer is free to create a buffer larger than that size. Under no circumstances, however, should the driver report the larger buffer size to DirectDraw.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a>



<a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a>



<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-_ddpixelformat">DDPIXELFORMAT</a>



<a href="/previous-versions/windows/hardware/drivers/ff549263(v=vs.85)">DdCreateSurface</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-videomemory">VIDEOMEMORY</a>