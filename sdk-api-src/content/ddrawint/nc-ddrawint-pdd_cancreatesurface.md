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
 

 

