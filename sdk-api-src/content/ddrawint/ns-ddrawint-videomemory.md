---
UID: NS:ddrawint._VIDEOMEMORY
title: VIDEOMEMORY (ddrawint.h)
description: The VIDEOMEMORY structure allows the driver to manage its display memory into heaps.
helpviewer_keywords: ["*LPVIDEOMEMORY","LPVIDEOMEMORY","LPVIDEOMEMORY structure pointer [Display Devices]","VIDEOMEMORY","VIDEOMEMORY structure [Display Devices]","ddrawint/LPVIDEOMEMORY","ddrawint/VIDEOMEMORY","ddstrcts_f00d50c3-df1a-46c6-8822-1be4a5cef837.xml","display.videomemory"]
old-location: display\videomemory.htm
tech.root: display
ms.assetid: a472a9f6-d85e-429b-9b0d-efce576b6330
ms.date: 12/05/2018
ms.keywords: '*LPVIDEOMEMORY, LPVIDEOMEMORY, LPVIDEOMEMORY structure pointer [Display Devices], VIDEOMEMORY, VIDEOMEMORY structure [Display Devices], ddrawint/LPVIDEOMEMORY, ddrawint/VIDEOMEMORY, ddstrcts_f00d50c3-df1a-46c6-8822-1be4a5cef837.xml, display.videomemory'
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
req.typenames: VIDEOMEMORY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VIDEOMEMORY
 - ddrawint/_VIDEOMEMORY
 - VIDEOMEMORY
 - ddrawint/VIDEOMEMORY
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
 - VIDEOMEMORY
---

# VIDEOMEMORY structure


## -description

The VIDEOMEMORY structure allows the driver to manage its display memory into heaps.

## -struct-fields

### -field dwFlags

Specifies a set of flags that describe this particular section of display memory. This member can be a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
VIDMEM_ISLINEAR

</td>
<td>
The display memory is a contiguous block of memory.

</td>
</tr>
<tr>
<td>
VIDMEM_ISRECTANGULAR

</td>
<td>
The display memory is rectangular.

</td>
</tr>
<tr>
<td>
VIDMEM_ISHEAP

</td>
<td>
This flag is reserved for system use and should be ignored by the driver.

</td>
</tr>
<tr>
<td>
VIDMEM_ISNONLOCAL

</td>
<td>
The heap resides in nonlocal (AGP) memory.

</td>
</tr>
<tr>
<td>
VIDMEM_ISWC

</td>
<td>
The driver has enabled write-combining on the display memory in this heap. Write-combining is a special caching mode in Pentium Pro-class processors that batches writes to the same cache line so they can be transferred in a single bus clock. Write-combining does not preserve ordering of the writes, a tradeoff that is usually acceptable for frame buffers. Refer to Intel documentation for more information about write-combining. This flag cannot be used unless the VIDMEM_ISNONLOCAL flag is also set.

</td>
</tr>
<tr>
<td>
VIDMEM_HEAPDISABLED

</td>
<td>
The Microsoft DirectDraw runtime uses this flag to turn off a heap when the heap's initialization has failed. This most likely occurs with an AGP heap. The driver should not set this bit.

</td>
</tr>
</table>

### -field fpStart

Points to the starting address of a memory range in the heap.

### -field fpEnd

Points to the ending address of a memory range if the heap is linear. This address is inclusive, that is, it specifies the last valid address in the range. Thus, the number of bytes specified by <b>fpStart</b> and <b>fpEnd</b> is (<b>fpEnd</b> - <b>fpStart </b>+ 1).

### -field dwWidth

Specifies the width in bytes of the section of memory pointed to by <b>fpStart</b>. This member should only be used to describe rectangular memory regions.

### -field ddsCapsAlt

Specifies a DDSCAPS structure in which the driver returns the capabilities for which this chunk of memory cannot be used when no other memory is found on the first pass.

### -field ddsCaps

Specifies a <a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a> structure in which the driver returns the capabilities for which this section of memory cannot be used.

### -field lpHeap

Reserved for system use and should be ignored by the driver.

### -field dwHeight

Specifies the height of the chunk of memory to which <b>fpStart</b> points. This member should only be used to describe rectangular memory regions.

## -remarks

On Microsoft Windows 2000 and later the data structure is called VIDEOMEMORY and on Windows 98/Me the data structure is called VIDMEM.

GDI allocates and passes an array of VIDEOMEMORY structures to the second call of the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a> function. The driver should fill in the appropriate members of each structure to describe each particular section of memory. The list provides a complete description of the driver's offscreen memory.

DirectDraw scans through to allocate its surfaces in the order the display memory heaps are listed. Heaps are managed in an array of VIDEOMEMORY structures. The memory allocated first will be the memory that is accessed first. The VIDEOMEMORY structure sets up certain starting points, and determines the amount of memory on the surface and what cannot be done with the surface. DirectDraw manages it by suballocating and deallocating memory, that is, creating and destroying surfaces under each heap's jurisdiction. Physical limits determine how to set up these attributes.

DirectDraw's heap manager makes two passes through the VIDEOMEMORY structures. The <b>ddsCaps</b> member indicates to DirectDraw what the memory in the heap cannot be used for on the first pass. For example, if the heap was just big enough for a back buffer, sprites could be excluded from being allocated on the first pass by setting the DSCAPS_OFFSCREENPLAIN flag in the <a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a> structure. That way, other surfaces would fill up with sprites, while preserving the back buffer for page flipping. The <b>ddsCapsAlt</b> member could be set to allow sprites on the second pass (by removing the DSCAPS_OFFSCREENPLAIN flag). This allows heaps to be used preferentially for their highest and best use, without ruling out alternative uses. By choosing the order of allocation carefully (for example, by listing the back buffer last), the need to sort by <b>ddsCaps</b> and <b>ddsCapsAlt</b> can sometimes be eliminated.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a>