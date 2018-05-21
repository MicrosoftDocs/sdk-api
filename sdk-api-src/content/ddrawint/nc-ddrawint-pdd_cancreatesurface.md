---
UID: NC:ddrawint.PDD_CANCREATESURFACE
title: PDD_CANCREATESURFACE
author: windows-driver-content
description: The CanCreateD3DBuffer callback function determines whether the driver can create a driver-level command or vertex buffer of the specified description.
old-location: display\cancreated3dbuffer.htm
old-project: display
ms.assetid: 94aace9f-0927-4b33-a9ea-79c27d5edea9
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CanCreateD3DBuffer, CanCreateD3DBuffer callback function [Display Devices], PDD_CANCREATESURFACE, PDD_CANCREATESURFACE callback, d3dfncs_c13b55de-ef44-4535-959c-dd61bfc3df10.xml, ddrawint/CanCreateD3DBuffer, display.cancreated3dbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ddrawint.h
api_name:
-	CanCreateD3DBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_CANCREATESURFACE callback function


## -description


The <b>CanCreateD3DBuffer</b> callback function determines whether the driver can create a driver-level command or vertex buffer of the specified description.


## -parameters




### -param Arg1








#### - lpCanCreateD3DBuffer

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550501">DD_CANCREATESURFACEDATA</a> structure. This structure contains the information required for the driver to determine whether a command or vertex buffer can be created.


## -returns



<b>CanCreateD3DBuffer</b> returns one of the following callback codes:




## -remarks



This callback is used only if the driver manages driver-level command and vertex buffers.

<b>CanCreateD3DBuffer</b> should check the surface description that the <b>lpDDSurfaceDesc</b> member of the DD_CANCREATESURFACEDATA structure at <b>lpCanCreateD3DBuffer</b> points to in order to determine whether the driver can support the format and capabilities of the requested buffer for the mode that the driver is currently in. The driver should return DD_OK in the <b>ddRVal</b> member of the same structure if it supports that type of buffer. Otherwise, it should return the DDERR_<i>Xxx</i> error code that best describes why it does not support the buffer.

This call has the same prototype as <a href="https://msdn.microsoft.com/015b94d7-427f-401d-b348-d4e9ec5cfe5d">DdCanCreateSurface</a>. The <b>CanCreateD3DBuffer</b> callback is used, however, when the surface in question has the DDSCAPS_EXECUTEBUFFER flag set in the <b>ddsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure.

The driver determines the type of buffer being requested by checking the <b>ddsCaps</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure for the following flags:

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




<a href="https://msdn.microsoft.com/8b012e65-b78b-41a4-ac05-d9be015b6ed8">CreateD3DBuffer</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550501">DD_CANCREATESURFACEDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/015b94d7-427f-401d-b348-d4e9ec5cfe5d">DdCanCreateSurface</a>
 

 

