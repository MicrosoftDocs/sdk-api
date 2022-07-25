---
UID: NC:ddrawint.PDD_CANCREATESURFACE
title: PDD_CANCREATESURFACE (ddrawint.h)
description: The CanCreateD3DBuffer callback function determines whether the driver can create a driver-level command or vertex buffer of the specified description.
helpviewer_keywords: ["CanCreateD3DBuffer","CanCreateD3DBuffer callback function [Display Devices]","PDD_CANCREATESURFACE","PDD_CANCREATESURFACE callback","d3dfncs_c13b55de-ef44-4535-959c-dd61bfc3df10.xml","ddrawint/CanCreateD3DBuffer","display.cancreated3dbuffer"]
old-location: display\cancreated3dbuffer.htm
tech.root: display
ms.assetid: 94aace9f-0927-4b33-a9ea-79c27d5edea9
ms.date: 12/05/2018
ms.keywords: CanCreateD3DBuffer, CanCreateD3DBuffer callback function [Display Devices], PDD_CANCREATESURFACE, PDD_CANCREATESURFACE callback, d3dfncs_c13b55de-ef44-4535-959c-dd61bfc3df10.xml, ddrawint/CanCreateD3DBuffer, display.cancreated3dbuffer
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_CANCREATESURFACE
 - ddrawint/PDD_CANCREATESURFACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - CanCreateD3DBuffer
---

## -description

The <b>CanCreateD3DBuffer</b> callback function determines whether the driver can create a driver-level command or vertex buffer of the specified description.

## -parameters

### -param unnamedParam1

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata">DD_CANCREATESURFACEDATA</a> structure. This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.

## -returns

<b>CanCreateD3DBuffer</b> returns a callback code.

## -remarks

This callback is used only if the driver manages driver-level command and vertex buffers.

<b>CanCreateD3DBuffer</b> should check the surface description that the <b>lpDDSurfaceDesc</b> member of the DD_CANCREATESURFACEDATA structure at <b>lpCanCreateD3DBuffer</b> points to in order to determine whether the driver can support the format and capabilities of the requested buffer for the mode that the driver is currently in. The driver should return DD_OK in the <b>ddRVal</b> member of the same structure if it supports that type of buffer. Otherwise, it should return the DDERR_<i>Xxx</i> error code that best describes why it does not support the buffer.

This call has the same prototype as <a href="/previous-versions/windows/hardware/drivers/ff549213(v=vs.85)">DdCanCreateSurface</a>. The <b>CanCreateD3DBuffer</b> callback is used, however, when the surface in question has the DDSCAPS_EXECUTEBUFFER flag set in the <b>ddsCaps</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure.

The driver determines the type of buffer being requested by checking the <b>ddsCaps</b> member of the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a> structure for the following flags:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSCAPS2_COMMANDBUFFER

</td>
<td>
The driver should allocate a command buffer.

</td>
</tr>
<tr>
<td>
DDSCAPS2_VERTEXBUFFER

</td>
<td>
The driver should allocate an explicit vertex buffer.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>    If neither flag is set, the driver should allocate an implicit vertex buffer. Implicit vertex buffers should not be placed in video memory since they are expected to be read/write. Only explicit vertex buffers with the DDSCAPS_WRITEONLY flag set can be safely placed in video memory.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_createsurface">CreateD3DBuffer</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_cancreatesurfacedata">DD_CANCREATESURFACEDATA</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surface_local">DD_SURFACE_LOCAL</a>



<a href="/previous-versions/windows/hardware/drivers/ff549213(v=vs.85)">DdCanCreateSurface</a>