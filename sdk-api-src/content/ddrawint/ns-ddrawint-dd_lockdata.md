---
UID: NS:ddrawint._DD_LOCKDATA
title: DD_LOCKDATA (ddrawint.h)
description: The DD_LOCKDATA structure contains information necessary to do a lock as defined by the Microsoft DirectDraw parameter structures.
helpviewer_keywords: ["*PDD_LOCKDATA","DD_LOCKDATA","DD_LOCKDATA structure [Display Devices]","ddrawint/DD_LOCKDATA","ddstrcts_8de05e54-e1e1-4773-982d-e48f7e051f7e.xml","display.dd_lockdata"]
old-location: display\dd_lockdata.htm
tech.root: display
ms.assetid: 46de3dbb-abdf-4518-b62d-891efa5a949b
ms.date: 12/05/2018
ms.keywords: '*PDD_LOCKDATA, DD_LOCKDATA, DD_LOCKDATA structure [Display Devices], ddrawint/DD_LOCKDATA, ddstrcts_8de05e54-e1e1-4773-982d-e48f7e051f7e.xml, display.dd_lockdata'
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
req.typenames: '*PDD_LOCKDATA, DD_LOCKDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_LOCKDATA
 - ddrawint/_DD_LOCKDATA
 - PDD_LOCKDATA
 - ddrawint/PDD_LOCKDATA
 - DD_LOCKDATA
 - ddrawint/DD_LOCKDATA
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
 - DD_LOCKDATA
---

# DD_LOCKDATA structure


## -description

The DD_LOCKDATA structure contains information necessary to do a lock as defined by the Microsoft DirectDraw parameter structures.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field lpDDSurface

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that describes the surface--in the case of <a href="/previous-versions/windows/hardware/drivers/ff568216(v=vs.85)">LockD3DBuffer</a>, a buffer--associated with the memory region to be locked down.

### -field bHasRect

Specifies whether the area in <b>rArea</b> is valid. A value of 0x00000001 indicates a valid area, 0x00000000 indicates an invalid area.

### -field rArea

Specifies a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the area on the surface to lock down.

### -field lpSurfData

Specifies the location in which the driver can return a pointer to the memory region that it locked down.

### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a> or <a href="/previous-versions/windows/hardware/drivers/ff568216(v=vs.85)">LockD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field Lock

Used by the DirectDraw API and should not be filled in by the driver.

### -field dwFlags

Specifies a bitmask that tells the driver how to perform the memory lockdown. This member is a bitwise OR of any of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDLOCK_DISCARDCONTENTS

</td>
<td>

<dl>
<dt>No assumptions are made about the contents of the surface or vertex buffer during this lock. This enables two things:</dt>
<dt>1. Microsoft Direct3D or the driver may provide an alternative memory area as the vertex buffer. This is useful when one plans to clear the contents of the vertex buffer and fill in new data.</dt>
<dt>2. Drivers sometimes store surface data in a reordered format. When the application locks the surface, the driver is forced to undo this surface data reordering before allowing the application to see the surface contents.</dt>
</dl>


This flag is a hint to the driver that it can skip the un-reordering process since the application plans to overwrite every single pixel in the surface or locked rectangle (and so erase any un-reordered pixels anyway). Applications should always set this flag when they intend to overwrite the entire surface or locked rectangle.

</td>
</tr>
<tr>
<td>
DDLOCK_DONOTWAIT

</td>
<td>
On <b>IDirectDrawSurface7</b> and higher interfaces, the default is DDLOCK_WAIT. If you wish to override the default and use time when the accelerator is busy (as denoted by the DDERR_WASSTILLDRAWING return code) then use this flag.

</td>
</tr>
<tr>
<td>
DDLOCK_EVENT

</td>
<td>
Set if an event handle is being passed to <b>Lock</b>, which triggers the event when it can return the surface memory pointer requested.

</td>
</tr>
<tr>
<td>
DDLOCK_HASVOLUMETEXTUREBOXRECT

</td>
<td>
The driver should return a valid memory pointer to the beginning of the subvolume texture specified in the rectangle (RECTL) in <b>rArea</b>. The driver obtains the front and back coordinates of the subvolume from the top 16 bits of the left and right coordinates (left and right members of RECTL) respectively. The left and right coordinates are constrained to the lower 16 bits. If no rectangle is specified, the driver should return a pointer to the top of the whole volume. This value is available in DirectX 8.1 and later.

</td>
</tr>
<tr>
<td>
DDLOCK_NODIRTYUPDATE

</td>
<td>

<dl>
<dt>Sent to the driver by the runtime after an application requests to lock down a memory region with the D3DLOCK_NO_DIRTY_UPDATE flag set. In this case, the driver should not consider the memory region that it locks down as dirty when the runtime calls the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_unlock">DdUnlock</a> function to update a surface that contains this region. Rather, the driver should only consider the regions specified in previous calls to its <a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a> function using the D3DDP2OP_ADDDIRTYRECT and D3DDP2OP_ADDDIRTYBOX enumerators as dirty. </dt>
<dt>By default, a lock on a surface adds a dirty region to that surface. </dt>
</dl>


</td>
</tr>
<tr>
<td>
DDLOCK_NOOVERWRITE

</td>
<td>
Used only with Direct3D vertex buffer locks. Indicates that no vertices that were referred to in <b>IDirect3DDevice7::DrawPrimitiveVB</b> and <b>IDirect3DDevice7::DrawIndexedPrimitiveVB</b> calls (described in the Direct3D SDK documentation) since the start of the frame (or the last lock without this flag) are modified during the lock. This can be useful when one is only appending data to the vertex buffer.

</td>
</tr>
<tr>
<td>
DDLOCK_NOSYSLOCK

</td>
<td>

<dl>
<dt>Indicates that a system-wide lock should not be taken when this surface is locked. This has several advantages when locking video memory surfaces, such as cursor responsiveness, ability to call more Microsoft Windows functions, and easier debugging. However, an application specifying this flag must comply with a number of conditions documented in the help file.</dt>
<dt>This flag cannot be specified when locking the primary.</dt>
</dl>


</td>
</tr>
<tr>
<td>
DDLOCK_OKTOSWAP

</td>
<td>
Same as DDLOCK_DISCARDCONTENTS.

</td>
</tr>
<tr>
<td>
DDLOCK_READONLY

</td>
<td>
The surface being locked will only be read from. On Windows 2000 and later, this flag is never set.

</td>
</tr>
<tr>
<td>
DDLOCK_SURFACEMEMORYPTR

</td>
<td>
The driver should return a valid memory pointer to the top of the rectangle specified in <b>rArea</b>. If no rectangle is specified, the driver should return a pointer to the top of the surface.

</td>
</tr>
<tr>
<td>
DDLOCK_WAIT

</td>
<td>
Set to indicate that <b>Lock</b> should wait until it can obtain a valid memory pointer before returning. If this bit is set, <b>Lock</b> never returns DDERR_WASSTILLDRAWING.

</td>
</tr>
<tr>
<td>
DDLOCK_WRITEONLY

</td>
<td>
The surface being locked will only be written to. On Windows 2000 and later, this flag is never set.

</td>
</tr>
</table>

### -field fpProcess

Specifies a pointer to a user-mode mapping of the driver's memory. The driver performs this mapping in <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mapmemory">DdMapMemory</a>. Windows 2000 and later only.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_lock">DdLock</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_mapmemory">DdMapMemory</a>



<a href="/previous-versions/windows/hardware/drivers/ff568216(v=vs.85)">LockD3DBuffer</a>