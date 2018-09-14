---
UID: NF:winddi.EngAssociateSurface
title: EngAssociateSurface function
author: windows-sdk-content
description: The EngAssociateSurface function marks a given surface as belonging to a specified device.
old-location: display\engassociatesurface.htm
tech.root: display
ms.assetid: 8cb6d4bf-67bd-4bfb-9605-eeb954fc590c
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: EngAssociateSurface, EngAssociateSurface function [Display Devices], display.engassociatesurface, gdifncs_6be89779-b79a-4620-b740-d702945464c5.xml, winddi/EngAssociateSurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngAssociateSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngAssociateSurface function


## -description


The <b>EngAssociateSurface</b> function marks a given surface as belonging to a specified device.


## -parameters




### -param hsurf

Handle to the surface or bitmap to be associated with <i>hdev</i>. This handle was returned by <a href="https://msdn.microsoft.com/51da3fbc-bf6e-47a9-8ee8-ebf34c23b66c">EngCreateBitmap</a> or <a href="https://msdn.microsoft.com/dc9d7154-30b9-4462-9161-6df03946308d">EngCreateDeviceBitmap</a>.


### -param hdev

Handle to the device with which the surface is to be associated. This is the GDI-created handle that was passed to the driver's <a href="https://msdn.microsoft.com/6343c6cc-f2f3-4776-a747-7a5b5cebef5f">DrvCompletePDEV</a> function.


### -param flHooks

Specifies the functions that the driver can hook from GDI. The driver must implement the corresponding function for every bit that it sets in <i>flHooks</i>. This member is a bitwise OR of any of the following values:  

<table>
<tr>
<th>Flag</th>
<th>Function to be hooked</th>
</tr>
<tr>
<td>
HOOK_ALPHABLEND

</td>
<td>

<a href="https://msdn.microsoft.com/fff3df30-cb29-4da3-97bc-dba5fbba1db5">DrvAlphaBlend</a>


</td>
</tr>
<tr>
<td>
HOOK_BITBLT

</td>
<td>

<a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>


</td>
</tr>
<tr>
<td>
HOOK_COPYBITS

</td>
<td>

<a href="https://msdn.microsoft.com/c2d42c7a-3d6e-416c-a194-2228cc1b0fd9">DrvCopyBits</a>


</td>
</tr>
<tr>
<td>
HOOK_FILLPATH

</td>
<td>

<a href="https://msdn.microsoft.com/6f499d08-d2a1-46d0-b931-e6c16c4e1d3a">DrvFillPath</a>


</td>
</tr>
<tr>
<td>
HOOK_GRADIENTFILL

</td>
<td>

<a href="https://msdn.microsoft.com/c8a51b5f-5509-4801-8432-c4d895cefbda">DrvGradientFill</a>


</td>
</tr>
<tr>
<td>
HOOK_LINETO

</td>
<td>

<a href="https://msdn.microsoft.com/e1e5dd93-444d-4176-9f7f-8aa220cddf78">DrvLineTo</a>


</td>
</tr>
<tr>
<td>
HOOK_MOVEPANNING

</td>
<td>
Obsolete

</td>
</tr>
<tr>
<td>
HOOK_PAINT

</td>
<td>
Obsolete

</td>
</tr>
<tr>
<td>
HOOK_PLGBLT

</td>
<td>

<a href="https://msdn.microsoft.com/5bd478f1-0c01-4d7f-9ed1-af84e5bbe773">DrvPlgBlt</a>


</td>
</tr>
<tr>
<td>
HOOK_STRETCHBLT

</td>
<td>

<a href="https://msdn.microsoft.com/3520533d-4e42-4abc-bc10-557c674caa33">DrvStretchBlt</a>


</td>
</tr>
<tr>
<td>
HOOK_STRETCHBLTROP

</td>
<td>

<a href="https://msdn.microsoft.com/eeaec7f4-2dfe-42a9-8789-a9ce11aec7b2">DrvStretchBltROP</a>


</td>
</tr>
<tr>
<td>
HOOK_STROKEANDFILLPATH

</td>
<td>

<a href="https://msdn.microsoft.com/92a04fe5-146d-4839-a854-1ac50705b447">DrvStrokeAndFillPath</a>


</td>
</tr>
<tr>
<td>
HOOK_STROKEPATH

</td>
<td>

<a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a>


</td>
</tr>
<tr>
<td>
HOOK_SYNCHRONIZE

</td>
<td>

<a href="https://msdn.microsoft.com/ed9b7db3-1409-4aa6-9ee1-9ece53e747a6">DrvSynchronize</a> or <a href="https://msdn.microsoft.com/717e0738-71a0-45e1-a479-337fab2998ab">DrvSynchronizeSurface</a> (either or both)

</td>
</tr>
<tr>
<td>
HOOK_SYNCHRONIZEACCESS

</td>
<td>
Obsolete

</td>
</tr>
<tr>
<td>
HOOK_TEXTOUT

</td>
<td>

<a href="https://msdn.microsoft.com/f2f61687-d833-4d09-8cd5-99e81436c1c1">DrvTextOut</a>


</td>
</tr>
<tr>
<td>
HOOK_TRANSPARENTBLT

</td>
<td>

<a href="https://msdn.microsoft.com/67e61a43-b962-4905-8876-9a0380848ed0">DrvTransparentBlt</a>


</td>
</tr>
</table>
 


## -returns



The return value is <b>TRUE</b> if the function is successful. Otherwise, the driver should send the information to the GDI function it is implementing, and return GDI's return value.




## -remarks



<b>EngAssociateSurface</b> can be used by printer drivers to implement "rules" or device fonts, or by display drivers to make use of special blt hardware.

If the surface identified by <i>hsurf</i> is a standard format bitmap, the driver can specify which output functions to the surface it will handle by setting bits in <i>flHooks</i>. Setting bits in <i>flHooks</i> causes particular output functions to be sent to the driver instead. This is referred to as hooking. If the driver does not hook a call, GDI will automatically manage the operation when a standard format bitmap is being drawn on. 

When the surface is associated, it assumes the default palette and style steps of the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. A surface must be associated before it is returned by <a href="https://msdn.microsoft.com/a838a44a-243c-4d0d-bda3-eec9a626cb53">DrvEnableSurface</a>.

By default, when a driver supports device bitmaps by implementing <a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>/<a href="https://msdn.microsoft.com/cb52b133-95c6-4a3d-b8b6-e1628a301542">DrvDeleteDeviceBitmap</a>, GDI does not automatically synchronize drawing calls to the device bitmap and to the primary surface. For example, GDI can call the driver's <a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a> function to draw to a device bitmap, while another thread is drawing to the primary surface by executing the driver's implementation of <a href="https://msdn.microsoft.com/f2f61687-d833-4d09-8cd5-99e81436c1c1">DrvTextOut</a>. The driver can even be called to draw to multiple device bitmaps at the same time.

After <a href="https://msdn.microsoft.com/a838a44a-243c-4d0d-bda3-eec9a626cb53">DrvEnableSurface</a> returns a handle to a primary surface, do not call <b>EngAssociateSurface</b> on that handle. Doing so can cause a bug check in certain circumstances. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=3100&amp;ID=330248">Microsoft Knowledge Base article 330248</a>.




## -see-also




<a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/6343c6cc-f2f3-4776-a747-7a5b5cebef5f">DrvCompletePDEV</a>



<a href="https://msdn.microsoft.com/c2d42c7a-3d6e-416c-a194-2228cc1b0fd9">DrvCopyBits</a>



<a href="https://msdn.microsoft.com/1f5f49ef-bf08-4311-9a1b-fdc37e6c2063">DrvCreateDeviceBitmap</a>



<a href="https://msdn.microsoft.com/cb52b133-95c6-4a3d-b8b6-e1628a301542">DrvDeleteDeviceBitmap</a>



<a href="https://msdn.microsoft.com/a838a44a-243c-4d0d-bda3-eec9a626cb53">DrvEnableSurface</a>



<a href="https://msdn.microsoft.com/6f499d08-d2a1-46d0-b931-e6c16c4e1d3a">DrvFillPath</a>



<a href="https://msdn.microsoft.com/e1e5dd93-444d-4176-9f7f-8aa220cddf78">DrvLineTo</a>



<a href="https://msdn.microsoft.com/3520533d-4e42-4abc-bc10-557c674caa33">DrvStretchBlt</a>



<a href="https://msdn.microsoft.com/92a04fe5-146d-4839-a854-1ac50705b447">DrvStrokeAndFillPath</a>



<a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a>



<a href="https://msdn.microsoft.com/ed9b7db3-1409-4aa6-9ee1-9ece53e747a6">DrvSynchronize</a>



<a href="https://msdn.microsoft.com/717e0738-71a0-45e1-a479-337fab2998ab">DrvSynchronizeSurface</a>



<a href="https://msdn.microsoft.com/f2f61687-d833-4d09-8cd5-99e81436c1c1">DrvTextOut</a>



<a href="https://msdn.microsoft.com/176f51c0-0075-4afb-8b5c-5d0b6b64a3ad">EngModifySurface</a>
 

 

