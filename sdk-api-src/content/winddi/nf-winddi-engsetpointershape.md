---
UID: NF:winddi.EngSetPointerShape
title: EngSetPointerShape function (winddi.h)
description: The EngSetPointerShape function sets the pointer shape for the calling driver.
helpviewer_keywords: ["EngSetPointerShape","EngSetPointerShape function [Display Devices]","display.engsetpointershape","gdifncs_468e4611-6696-4535-af00-014999695d6e.xml","winddi/EngSetPointerShape"]
old-location: display\engsetpointershape.htm
tech.root: display
ms.assetid: 9b3a1e44-f3c6-4160-8d5d-d114511ad201
ms.date: 12/05/2018
ms.keywords: EngSetPointerShape, EngSetPointerShape function [Display Devices], display.engsetpointershape, gdifncs_468e4611-6696-4535-af00-014999695d6e.xml, winddi/EngSetPointerShape
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
 - EngSetPointerShape
 - winddi/EngSetPointerShape
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngSetPointerShape
---

# EngSetPointerShape function


## -description

The <b>EngSetPointerShape</b> function sets the pointer shape for the calling driver.

## -parameters

### -param pso [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param psoMask [in]

Pointer to a SURFOBJ structure that defines the AND-XOR mask to apply to the pointer bitmap. The top half of the bitmap specifies the monochrome AND mask and the bottom half specifies the monochrome XOR mask. The pointer is the same width and half the height of the mask to which <i>psoMask</i> points. There are no implicit constraints on pointer sizes, but optimal pointer sizes are 32 x 32, 48 x 48, and 64 x 64 pixels. If this parameter is <b>NULL</b>, the pointer is transparent.

### -param psoColor [in]

Pointer to a SURFOBJ structure that defines the colors for a color pointer. This bitmap is the same width and half the height of the bitmap to which <i>psoMask</i> points, and is in the same color format as the surface to which <i>pso</i> points. If this parameter is <b>NULL</b>, the pointer is monochrome.

### -param pxlo [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that defines the colors in <i>psoColor</i>.

### -param xHot [in]

Specifies the x coordinate of the pointer's hot spot relative to its upper-left pixel. The pixel indicated by the hot spot should be positioned at the new pointer position.

### -param yHot [in]

Specifies the y coordinate of the pointer's hot spot relative to its upper-left pixel. The pixel indicated by the hot spot should be positioned at the new pointer position.

### -param x [in]

Specifies the x coordinates of the new pointer position.

### -param y [in]

Specifies the y coordinates of the new pointer position.

### -param prcl [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure. If non-<b>NULL</b>, the driver has provided a rectangle that bounds all pixels affected by the pointer on the display. GDI avoids drawing on this rectangle without first moving the pointer out of the way.

### -param fl [in]

Specifies a set of flags that GDI should use to process this call. This parameter can be one or more of the following predefined values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
SPS_ANIMATESTART

</td>
<td>
GDI should be prepared to receive a series of similarly-sized pointer shapes that will comprise an animated pointer effect.

</td>
</tr>
<tr>
<td>
SPS_ANIMATEUPDATE

</td>
<td>
GDI should draw the next pointer shape in the animated series.

</td>
</tr>
<tr>
<td>
SPS_CHANGE

</td>
<td>
GDI is requested to change the pointer shape.

</td>
</tr>
</table>

## -returns

<b>EngSetPointerShape</b> returns one of the following values:

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
GDI accepts the shape. GDI does not read from or write to the rectangle written at <i>prcl</i> without first moving the pointer out of the way.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPS_ERROR</b></dt>
</dl>
</td>
<td width="60%">
GDI normally supports this shape, but failed for unusual reasons.

</td>
</tr>
</table>

## -remarks

The driver can call <b>EngSetPointerShape</b> to have GDI manage a software cursor.

There are two parts to the monochrome bitmap to which <i>psoMask</i> points. The first part defines the AND mask for the pointer while the second part defines the XOR mask. Taken together, these masks provide two bits of information for each pixel of the pointer image. The following truth table determines what GDI draws on the display for different values in the AND and XOR masks:

<table>
<tr>
<th>AND value</th>
<th>XOR value</th>
<th>Resultant Pixel</th>
</tr>
<tr>
<td>
0

</td>
<td>
0

</td>
<td>
White

</td>
</tr>
<tr>
<td>
0

</td>
<td>
1

</td>
<td>
Black

</td>
</tr>
<tr>
<td>
1

</td>
<td>
0

</td>
<td>
No change in pixel 

</td>
</tr>
<tr>
<td>
1

</td>
<td>
1

</td>
<td>
Pixel color is inverted

</td>
</tr>
</table>
 

This mechanism supplies a black and white image while allowing for transparency and inversion of the pixels that make up the pointer.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvsetpointershape">DrvSetPointerShape</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmovepointer">EngMovePointer</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>