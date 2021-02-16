---
UID: NS:ddrawint._DD_D3DBUFCALLBACKS
title: DD_D3DBUFCALLBACKS (ddrawint.h)
description: The DD_D3DBUFCALLBACKS structure is used only by drivers that implement driver level allocation of command and vertex buffers.
helpviewer_keywords: ["*PDD_D3DBUFCALLBACKS","DD_D3DBUFCALLBACKS","DD_D3DBUFCALLBACKS structure [Display Devices]","PDD_D3DBUFCALLBACKS","PDD_D3DBUFCALLBACKS structure pointer [Display Devices]","ddrawint/DD_D3DBUFCALLBACKS","ddrawint/PDD_D3DBUFCALLBACKS","ddstrcts_cfe891c1-2660-460f-ac58-79f243ee902e.xml","display.dd_d3dbufcallbacks"]
old-location: display\dd_d3dbufcallbacks.htm
tech.root: display
ms.assetid: 59fa4043-6238-49f7-b9d6-58c1f215865a
ms.date: 12/05/2018
ms.keywords: '*PDD_D3DBUFCALLBACKS, DD_D3DBUFCALLBACKS, DD_D3DBUFCALLBACKS structure [Display Devices], PDD_D3DBUFCALLBACKS, PDD_D3DBUFCALLBACKS structure pointer [Display Devices], ddrawint/DD_D3DBUFCALLBACKS, ddrawint/PDD_D3DBUFCALLBACKS, ddstrcts_cfe891c1-2660-460f-ac58-79f243ee902e.xml, display.dd_d3dbufcallbacks'
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
req.typenames: DD_D3DBUFCALLBACKS, *PDD_D3DBUFCALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_D3DBUFCALLBACKS
 - ddrawint/_DD_D3DBUFCALLBACKS
 - PDD_D3DBUFCALLBACKS
 - ddrawint/PDD_D3DBUFCALLBACKS
 - DD_D3DBUFCALLBACKS
 - ddrawint/DD_D3DBUFCALLBACKS
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
 - DD_D3DBUFCALLBACKS
---

# DD_D3DBUFCALLBACKS structure


## -description

The DD_D3DBUFCALLBACKS structure is used only by drivers that implement driver level allocation of command and vertex buffers.

## -struct-fields

### -field dwSize

Specifies the size in bytes of this DD_D3DBUFCALLBACKS structure.

### -field dwFlags

Reserved.

### -field CanCreateD3DBuffer

Points to the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_cancreatesurface">CanCreateD3DBuffer</a> callback.

### -field CreateD3DBuffer

Points to the driver's <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a> callback.

### -field DestroyD3DBuffer

Points to the driver's <a href="/previous-versions/windows/hardware/drivers/ff552754(v=vs.85)">DestroyD3DBuffer</a> callback.

### -field LockD3DBuffer

Points to the driver's <a href="/previous-versions/windows/hardware/drivers/ff568216(v=vs.85)">LockD3DBuffer</a> callback.

### -field UnlockD3DBuffer

Points to the driver's <a href="/previous-versions/windows/hardware/drivers/ff570106(v=vs.85)">UnlockD3DBuffer</a> callback.

## -remarks

Drivers that manage their own command and vertex buffers must fill out a DD_D3DBUFCALLBACKS structure and point the <b>lpD3DBufCallbacks</b> member of <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_halinfo">DD_HALINFO</a> to it. 

The driver must also support the callback functions reported in the DD_D3DBUFCALLBACKS structure. These <i>XxxD3DBuffer</i> callbacks are each analogous to the <i>DdXxxSurface</i> callback of similar name; they have the same prototypes and are called with the same input parameters. These new callbacks are called only when the surface in question has the DDSCAPS_EXECUTEBUFFER flag set in the surface caps. The buffer creation flags are DDSCAPS_WRITEONLY, DDSCAPS2_VERTEXBUFFER and DDSCAPS2_COMMANDBUFFER. 

The driver determines the type of buffer being requested by checking the <b>ddsCaps</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure that is passed to <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_cancreatesurface">CanCreateD3DBuffer</a> and <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a> for the following flags:

<ul>
<li>
DDSCAPS_VERTEXBUFFER

Indicates that the driver should allocate an explicit vertex buffer.

</li>
<li>
DDSCAPS_COMMANDBUFFER

Indicates that the driver should allocate a command buffer. 

</li>
<li>
The absence of both these flags 

Indicates that the driver should allocate an implicit vertex buffer.

</li>
</ul>
Implicit vertex buffers should not be placed in video memory because they are expected to be read/write. Only explicit vertex buffers with the DDSCAPS_WRITEONLY flag set can be safely placed in video memory.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_cancreatesurface">CanCreateD3DBuffer</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_halinfo">DD_HALINFO</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>



<a href="/previous-versions/windows/hardware/drivers/ff552754(v=vs.85)">DestroyD3DBuffer</a>



<a href="/previous-versions/windows/hardware/drivers/ff568216(v=vs.85)">LockD3DBuffer</a>



<a href="/previous-versions/windows/hardware/drivers/ff570106(v=vs.85)">UnlockD3DBuffer</a>