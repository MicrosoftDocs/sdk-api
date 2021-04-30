---
UID: NF:winddi.DrvSetPointerShape
title: DrvSetPointerShape function (winddi.h)
description: The DrvSetPointerShape function is used to request the driver to take the pointer off the display, if the driver has drawn it there; to attempt to set a new pointer shape; and to put the new pointer on the display at a specified position.
helpviewer_keywords: ["DrvSetPointerShape","DrvSetPointerShape function [Display Devices]","ddifncs_86472b92-edfc-4811-8b35-e690136a2430.xml","display.drvsetpointershape","winddi/DrvSetPointerShape"]
old-location: display\drvsetpointershape.htm
tech.root: display
ms.assetid: 3cc186df-572b-48ed-ac0b-56c8d91a9794
ms.date: 12/05/2018
ms.keywords: DrvSetPointerShape, DrvSetPointerShape function [Display Devices], ddifncs_86472b92-edfc-4811-8b35-e690136a2430.xml, display.drvsetpointershape, winddi/DrvSetPointerShape
req.header: winddi.h
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
 - DrvSetPointerShape
 - winddi/DrvSetPointerShape
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvSetPointerShape
---

# DrvSetPointerShape function


## -description

The <b>DrvSetPointerShape</b> function is used to request the driver to take the pointer off the display, if the driver has drawn it there; to attempt to set a new pointer shape; and to put the new pointer on the display at a specified position.

## -parameters

### -param pso [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param psoMask [in]

Pointer to the SURFOBJ structure that defines the AND-XOR mask. (The AND-XOR mask is described in <a href="/windows-hardware/drivers/display/drawing-monochrome-pointers">Drawing Monochrome Pointers</a>.) The dimensions of this bitmap determine the size of the pointer. There are no implicit constraints on pointer sizes, but optimal pointer sizes are 32 x 32, 48 x 48, and 64 x 64 pixels. If this parameter is <b>NULL</b>, the pointer is transparent.

### -param psoColor [in]

Pointer to the SURFOBJ structure that defines the colors for a color pointer. If this parameter is <b>NULL</b>, the pointer is monochrome. The pointer bitmap has the same width as <i>psoMask</i> and half the height.

### -param pxlo [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that defines the colors in <i>psoColor</i>.

### -param xHot [in]

Specify the <i>x</i> position of the pointer's hot spot relative to its upper-left pixel. The pixel indicated by the hot spot should be positioned at the new pointer position.

### -param yHot [in]

Specify the <i>y</i> position of the pointer's hot spot relative to its upper-left pixel. The pixel indicated by the hot spot should be positioned at the new pointer position.

### -param x [in]

Specify the x-coordinate of the new pointer position.

### -param y [in]

Specify the y-coordinate of the new pointer position.

### -param prcl [in]

Specifies the <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that indicates the location in which the driver should write a rectangle that specifies a tight bound for the visible portion of the pointer.

### -param fl [in]

Specifies an extensible set of flags. The driver should decline the call if any flags are set that it does not understand. This parameter can be one or more of the following predefined values, and one or more driver-defined values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SPS_ALPHA

</td>
<td>
The pointer has per-pixel alpha values. 

</td>
</tr>
<tr>
<td>
SPS_ANIMATESTART

</td>
<td>
The driver should be prepared to receive a series of similarly-sized pointer shapes that will comprise an animated pointer effect.

</td>
</tr>
<tr>
<td>
SPS_ANIMATEUPDATE

</td>
<td>
The driver should draw the next pointer shape in the animated series.

</td>
</tr>
<tr>
<td>
SPS_ASYNCCHANGE

</td>
<td>
This flag is obsolete. For legacy drivers, the driver should accept the change only if it is capable of changing the pointer shape in the hardware while other drawing is underway on the device. GDI uses this option only if the now obsolete GCAPS_ASYNCCHANGE flag is set in the <b>flGraphicsCaps</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

</td>
</tr>
<tr>
<td>
SPS_CHANGE

</td>
<td>
The driver is requested to change the pointer shape.

</td>
</tr>
<tr>
<td>
SPS_FREQMASK

</td>
<td>
The driver is requested to render a mouse trail, updating the image as many times per millisecond as indicated in the expression <i>fl</i> &amp; SPS_FREQMASK. A driver that is capable of rendering mouse trails must have the GCAPS2_MOUSETRAILS flag set in the <b>flGraphicsCaps2</b> member of its <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

</td>
</tr>
<tr>
<td>
SPS_LENGTHMASK

</td>
<td>
The driver is requested to render a mouse trail of length indicated by the expression <i>fl</i> &amp; SPS_LENGTHMASK. (A mouse trail of length <i>N</i> is made up of <i>N</i> + 1 cursor images.) A driver that is capable of rendering mouse trails must have the GCAPS2_MOUSETRAILS flag set in the <b>flGraphicsCaps2</b> member of its <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

</td>
</tr>
</table>

## -returns

The return value can be one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPS_ACCEPT_EXCLUDE</b></dt>
</dl>
</td>
<td width="60%">
Is obsolete. GDI will disable the driver's pointer and revert to software simulation if the driver returns this value.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPS_ACCEPT_NOEXCLUDE</b></dt>
</dl>
</td>
<td width="60%">
The driver accepts the shape. The shape is supported in hardware and GDI is not concerned about other drawings overwriting the pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPS_DECLINE</b></dt>
</dl>
</td>
<td width="60%">
The driver does not support the shape, so GDI must simulate it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPS_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The driver normally supports this shape, but failed for unusual reasons.

</td>
</tr>
</table>

## -remarks

<b>DrvSetPointerShape</b> is optional for display drivers. If this function is implemented, however, <a href="/windows/desktop/api/winddi/nf-winddi-drvmovepointer">DrvMovePointer</a> must also be implemented.

The <b>iUniq</b> members of the SURFOBJ structures to which <i>psoMask</i> and <i>psoColor</i> point are unique for unique pointers. The driver can use this information in conjunction with these structures' unique <b>dhsurf</b> handles as cache keys for cursor caching.

When SPS_ALPHA is set in the <i>fl</i> parameter, <i>psoMask</i> is <b>NULL</b> and <i>psoColor</i> points to a 32bpp BGRA surface. The per-pixel alpha value indicates the opacity of the corresponding pointer pixel with the desktop pixel underneath. The source alpha format is premultiplied; that is, each of the color channels of the source surface has already been premultiplied with the corresponding alpha value, thus eliminating a multiply operation at the time of the blend.

Default alpha cursors are largely black and white with a large range of alpha values; however, there is no color restriction since applications can specify arbitrary cursors themselves. Typical alpha pointer sizes are approximately 8 pixels larger in dimension than typical pointers without alpha. This accommodates the shadow effect, which is accomplished by a blurring filter that expands the resulting pointer bitmap shape. The vast majority of pointers will be 64x64 pixel bitmaps or smaller.

The driver indicates its ability to handle pointers with per-pixel alpha values by setting the GCAPS2_ALPHACURSOR flag in the <b>flGraphicsCaps2</b> member of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure returned by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvmovepointer">DrvMovePointer</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>