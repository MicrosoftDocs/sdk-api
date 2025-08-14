---
UID: NF:winddi.EngAssociateSurface
title: EngAssociateSurface function (winddi.h)
description: The EngAssociateSurface function marks a given surface as belonging to a specified device.
helpviewer_keywords: ["EngAssociateSurface","EngAssociateSurface function [Display Devices]","display.engassociatesurface","gdifncs_6be89779-b79a-4620-b740-d702945464c5.xml","winddi/EngAssociateSurface"]
old-location: display\engassociatesurface.htm
tech.root: display
ms.assetid: 8cb6d4bf-67bd-4bfb-9605-eeb954fc590c
ms.date: 12/05/2018
ms.keywords: EngAssociateSurface, EngAssociateSurface function [Display Devices], display.engassociatesurface, gdifncs_6be89779-b79a-4620-b740-d702945464c5.xml, winddi/EngAssociateSurface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngAssociateSurface
 - winddi/EngAssociateSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngAssociateSurface
---

# EngAssociateSurface function


## -description

The <b>EngAssociateSurface</b> function marks a given surface as belonging to a specified device.

## -parameters

### -param hsurf

Handle to the surface or bitmap to be associated with <i>hdev</i>. This handle was returned by <a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a> or <a href="/windows/desktop/api/winddi/nf-winddi-engcreatedevicebitmap">EngCreateDeviceBitmap</a>.

### -param hdev

Handle to the device with which the surface is to be associated. This is the GDI-created handle that was passed to the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a> function.

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

<a href="/windows/desktop/api/winddi/nf-winddi-drvalphablend">DrvAlphaBlend</a>


</td>
</tr>
<tr>
<td>
HOOK_BITBLT

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>


</td>
</tr>
<tr>
<td>
HOOK_COPYBITS

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a>


</td>
</tr>
<tr>
<td>
HOOK_FILLPATH

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvfillpath">DrvFillPath</a>


</td>
</tr>
<tr>
<td>
HOOK_GRADIENTFILL

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvgradientfill">DrvGradientFill</a>


</td>
</tr>
<tr>
<td>
HOOK_LINETO

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvlineto">DrvLineTo</a>


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

<a href="/windows/desktop/api/winddi/nf-winddi-drvplgblt">DrvPlgBlt</a>


</td>
</tr>
<tr>
<td>
HOOK_STRETCHBLT

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>


</td>
</tr>
<tr>
<td>
HOOK_STRETCHBLTROP

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchbltrop">DrvStretchBltROP</a>


</td>
</tr>
<tr>
<td>
HOOK_STROKEANDFILLPATH

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokeandfillpath">DrvStrokeAndFillPath</a>


</td>
</tr>
<tr>
<td>
HOOK_STROKEPATH

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokepath">DrvStrokePath</a>


</td>
</tr>
<tr>
<td>
HOOK_SYNCHRONIZE

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronize">DrvSynchronize</a> or <a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronizesurface">DrvSynchronizeSurface</a> (either or both)

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

<a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>


</td>
</tr>
<tr>
<td>
HOOK_TRANSPARENTBLT

</td>
<td>

<a href="/windows/desktop/api/winddi/nf-winddi-drvtransparentblt">DrvTransparentBlt</a>


</td>
</tr>
</table>

## -returns

The return value is <b>TRUE</b> if the function is successful. Otherwise, the driver should send the information to the GDI function it is implementing, and return GDI's return value.

## -remarks

<b>EngAssociateSurface</b> can be used by printer drivers to implement "rules" or device fonts, or by display drivers to make use of special blt hardware.

If the surface identified by <i>hsurf</i> is a standard format bitmap, the driver can specify which output functions to the surface it will handle by setting bits in <i>flHooks</i>. Setting bits in <i>flHooks</i> causes particular output functions to be sent to the driver instead. This is referred to as hooking. If the driver does not hook a call, GDI will automatically manage the operation when a standard format bitmap is being drawn on. 

When the surface is associated, it assumes the default palette and style steps of the <a href="/windows-hardware/drivers/">PDEV</a>. A surface must be associated before it is returned by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>.

By default, when a driver supports device bitmaps by implementing <a href="/windows/desktop/api/winddi/nf-winddi-drvcreatedevicebitmap">DrvCreateDeviceBitmap</a>/<a href="/windows/desktop/api/winddi/nf-winddi-drvdeletedevicebitmap">DrvDeleteDeviceBitmap</a>, GDI does not automatically synchronize drawing calls to the device bitmap and to the primary surface. For example, GDI can call the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a> function to draw to a device bitmap, while another thread is drawing to the primary surface by executing the driver's implementation of <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>. The driver can even be called to draw to multiple device bitmaps at the same time.

After <a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a> returns a handle to a primary surface, do not call <b>EngAssociateSurface</b> on that handle. Doing so can cause a bug check in certain circumstances. For more information, see <a href="https://support.microsoft.com/?kbid&amp;ID=330248">Microsoft Knowledge Base article 330248</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvbitblt">DrvBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvcopybits">DrvCopyBits</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvcreatedevicebitmap">DrvCreateDeviceBitmap</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvdeletedevicebitmap">DrvDeleteDeviceBitmap</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvfillpath">DrvFillPath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvlineto">DrvLineTo</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstretchblt">DrvStretchBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokeandfillpath">DrvStrokeAndFillPath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstrokepath">DrvStrokePath</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronize">DrvSynchronize</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronizesurface">DrvSynchronizeSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmodifysurface">EngModifySurface</a>