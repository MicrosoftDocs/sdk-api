---
UID: NC:ddrawint.PDD_CREATESURFACE
title: PDD_CREATESURFACE
author: windows-sdk-content
description: The CreateD3DBuffer callback function is used to create a driver-level command or vertex buffer of the specified description.
old-location: display\created3dbuffer.htm
tech.root: display
ms.assetid: 8b012e65-b78b-41a4-ac05-d9be015b6ed8
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: CreateD3DBuffer, CreateD3DBuffer callback function [Display Devices], PDD_CREATESURFACE, PDD_CREATESURFACE callback, d3dfncs_065c964d-8e17-4ec1-9b9a-c74d2f91aa27.xml, ddrawint/CreateD3DBuffer, display.created3dbuffer
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - CreateD3DBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_CREATESURFACE callback function


## -description


The <i>CreateD3DBuffer</i> callback function is used to create a driver-level command or vertex buffer of the specified description.


## -parameters




### -param Arg1








#### - lpCreateD3DBuffer

Points to a <a href="https://msdn.microsoft.com/5a3b4267-43b4-44dc-abad-cb3f3d07f30e">DD_CREATESURFACEDATA</a> structure that contains the information required to create the buffer.


## -returns



<i>CreateD3DBuffer</i> returns one of the following callback codes:




## -remarks



This callback is used only if the driver manages driver-level command and vertex buffers.

By default, the driver is not notified when a primary surface is created on Windows 2000 and later versions. However, if the driver supports the GUID_NTPrivateDriverCaps GUID in a <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> call and the DDHAL_PRIVATECAP_NOTIFYPRIMARYCREATION flag is set in the <b>dwPrivateCaps</b> member of the <a href="https://msdn.microsoft.com/d802b080-cf94-400a-96c4-e765008dfc8a">DD_NTPRIVATEDRIVERCAPS</a> structure, then the driver is notified.

The pitch must be returned in the <b>lPitch</b> member of both the <a href="https://msdn.microsoft.com/11e0a6b9-16b9-4fc3-8e17-776f56c12196">DD_SURFACE_GLOBAL</a> and <a href="https://msdn.microsoft.com/d6656bae-9f90-497b-82d5-be4be3213687">DDSURFACEDESC</a> structures. For linear memory, the driver should set <b>dwBlockSizeX</b> to the size, in bytes, of the memory region and set <b>dwBlockSizeY</b> to 1. Both are members of the DD_SURFACE_GLOBAL structure.

This call has the same prototype as <a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a>. The <i>CreateD3DBuffer</i> callback is used instead when the surface in question has the DDSCAPS_EXECUTEBUFFER flag set in the <b>ddsCaps</b> member of the <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure. The buffer creation flags are DDSCAPS_WRITEONLY, DDSCAPS2_VERTEXBUFFER and DDSCAPS2_COMMANDBUFFER. 

The driver determines the type of buffer being requested by checking the <b>ddsCaps</b> member of the DD_SURFACE_LOCAL structure for the following flags:

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
 

<div class="alert"><b>Note</b>    If neither flag is set, the driver should allocate an implicit vertex buffer. Implicit vertex buffers should not be placed in video memory because they are expected to be read/write. Only explicit vertex buffers with the DDSCAPS_WRITEONLY flag set can be safely placed in video memory.</div>
<div> </div>
The driver can allocate the buffer memory itself or it can request that Microsoft DirectDraw perform the memory management. If the driver performs the allocation, it must write a valid pointer to the memory in the <b>fpVidMem</b> member of the <a href="https://msdn.microsoft.com/11e0a6b9-16b9-4fc3-8e17-776f56c12196">DD_SURFACE_GLOBAL</a>  structure.

Alternatively, the driver can request that DirectDraw allocate the buffer by returning one of the following values in <b>fpVidMem</b>:

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
DirectDraw should allocate the buffer memory from offscreen memory.

</td>
</tr>
<tr>
<td>
DDHAL_PLEASEALLOC_USERMEM

</td>
<td>
DirectDraw should allocate the buffer memory from user memory. The driver must also return the size, in bytes, of the memory region in <b>dwUserMemSize</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d6656bae-9f90-497b-82d5-be4be3213687">DDSURFACEDESC</a>



<a href="https://msdn.microsoft.com/5a3b4267-43b4-44dc-abad-cb3f3d07f30e">DD_CREATESURFACEDATA</a>



<a href="https://msdn.microsoft.com/d802b080-cf94-400a-96c4-e765008dfc8a">DD_NTPRIVATEDRIVERCAPS</a>



<a href="https://msdn.microsoft.com/11e0a6b9-16b9-4fc3-8e17-776f56c12196">DD_SURFACE_GLOBAL</a>



<a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a>



<a href="https://msdn.microsoft.com/45c793ed-34e8-4a15-91f4-9a258c1842fd">DdCreateSurface</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

