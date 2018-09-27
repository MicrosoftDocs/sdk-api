---
UID: NF:winddi.EngStretchBltROP
title: EngStretchBltROP function
author: windows-sdk-content
description: The EngStretchBltROP function performs a stretching bit-block transfer using a ROP.
old-location: display\engstretchbltrop.htm
tech.root: display
ms.assetid: d353fab2-ba5d-42a5-8ce7-04fdc731f6ee
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EngStretchBltROP, EngStretchBltROP function [Display Devices], display.engstretchbltrop, gdifncs_344d6d6a-0691-4dfd-92fa-918b2c4c63b8.xml, winddi/EngStretchBltROP
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
 - EngStretchBltROP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngStretchBltROP function


## -description


The <b>EngStretchBltROP</b> function performs a stretching bit-block transfer using a <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">ROP</a>.


## -parameters




### -param psoDest

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface on which to draw.


### -param psoSrc

Pointer to a SURFOBJ structure that describes the source surface for the bit-block transfer.


### -param psoMask

Pointer to a SURFOBJ structure that defines a mask for the source surface. The mask is defined by a logic map, which is a bitmap with 1 bit per pixel. Typically, a mask limits the area that is to be modified in the destination surface. This mask should always be the same size as the source surface.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure that limits the area to be modified in the destination. The <b>CLIPOBJ_</b><i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles.

Whenever possible, GDI simplifies the clipping involved. However, unlike <a href="https://msdn.microsoft.com/e99dbe54-485b-4a56-9956-2965f04020db">EngBitBlt</a>, <b>EngStretchBltROP</b> can be called with a single clipping rectangle. This prevents rounding errors in clipping the output.


### -param pxlo

Pointer to a <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure that specifies how color indices are to be translated between the source and target surfaces.

This XLATEOBJ structure can also be queried to find the RGB color for any source index. A high quality stretching bit-block transfer will need to interpolate colors in some cases.


### -param pca

Pointer to a COLORADJUSTMENT structure that defines the color adjustment values to be applied to the source bitmap before stretching the bits. For more information see the Windows SDK documentation.


### -param pptlHTOrg

Pointer to a <a href="https://msdn.microsoft.com/68cd23d7-7898-4132-abfe-4dda527889b9">POINTL</a> structure that defines the origin of the halftone brush on the destination surface. When using halftone brushes, GDI aligns the upper left pixel of the brush's pattern at this point and repeats the brush according to its dimensions. GDI ignores this parameter if the <i>rop4</i> parameter does not require a pattern.


### -param prclDest [in]

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the rectangular area to be modified. This rectangle is specified in the coordinate system of the destination surface and is defined by two points: upper left and lower right. The two points that define the rectangle are not always well ordered, meaning the coordinates of the second point are not necessarily larger than those of the first point. If the destination rectangle is not well ordered, GDI makes it so.

The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the copy.

<b>EngStretchBltROP</b> must never be called with an empty destination rectangle.


### -param prclSrc [in]

Pointer to a RECTL structure that defines the area to be copied. This rectangle is specified in the coordinate system of the source surface and is defined by two points: upper left and lower right. The two points that define the rectangle are always well ordered.

The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the copy.

This rectangle maps to the rectangle to which <i>prclDest</i> points.

<b>EngStretchBltROP</b> must never be called with an empty source rectangle.


### -param pptlMask

Pointer to a POINTL structure that defines the pixel in the mask to which <i>prclMask</i> points. This pixel corresponds to the upper-left pixel in the source rectangle to which <i>prclSrc</i> points. This parameter is ignored if no mask is specified; that is, GDI ignores <i>pptlMask</i> when <i>prclMask</i> is <b>NULL</b>.


### -param iMode [in]

Specifies how source pixels are combined to get output pixels. The HALFTONE mode is slower than the other modes, but produces higher quality images. This parameter can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
BLACKONWHITE

</td>
<td>
On a shrinking bit-block transfer, GDI combines pixels with a Boolean AND operation. On a stretching bit-block transfer, pixels are replicated.

</td>
</tr>
<tr>
<td>
COLORONCOLOR

</td>
<td>
On a shrinking bit-block transfer, GDI ignores enough pixels so that pixels need not be combined. On a stretching bit-block transfer, pixels are replicated.

</td>
</tr>
<tr>
<td>
HALFTONE

</td>
<td>
GDI uses groups of pixels in the output surface to best approximate the color or gray level of the input.

</td>
</tr>
<tr>
<td>
WHITEONBLACK

</td>
<td>
On a shrinking bit-block transfer, pixels should be combined with a Boolean OR operation. On a stretching bit-block transfer, pixels should be replicated.

</td>
</tr>
</table>
 


### -param pbo

Pointer to the <a href="https://msdn.microsoft.com/81216bee-d13f-4880-a839-337a247a6c82">BRUSHOBJ</a> structure to be used to define the pattern for the bit-block transfer. GDI's <a href="https://msdn.microsoft.com/3f3e5acb-f984-4571-9555-f6b383ddb6a7">BRUSHOBJ_pvGetRbrush</a> service routine retrieves the device's realization of the brush. GDI ignores this parameter if the <i>rop4</i> parameter does not require a pattern.


### -param rop4 [in]

Represents a raster operation that defines how the mask, pattern, source, and destination pixels are combined to write an output pixel to the destination surface.

This is a quaternary raster operation, which is a natural extension of the usual ternary Rop3 operation. A Rop4 has 16 relevant bits, which are similar to the 8 defining bits of a Rop3. (The other redundant bits of the Rop3 are ignored.) The simplest way to implement a Rop4 is to consider its 2 bytes separately. The lower byte specifies a Rop3 that should be computed wherever the mask to which <i>psoMask</i> points is 1. The high byte specifies a Rop3 that can be computed and applied wherever the mask is zero.


## -returns



<b>EngStretchBltROP</b> returns <b>TRUE</b> upon success. Otherwise, it reports an error and returns <b>FALSE</b>.




## -remarks



The driver should call <b>EngStretchBltROP</b> if it has hooked <a href="https://msdn.microsoft.com/eeaec7f4-2dfe-42a9-8789-a9ce11aec7b2">DrvStretchBltROP</a> but cannot support all operations.

The mapping is defined by <i>prclSrc</i> and <i>prclDest</i>. The points specified in <i>prclDest</i> and <i>prclSrc</i> lie on integer coordinates that correspond to pixel centers. A rectangle defined by two such points is considered to be a geometric rectangle with two vertices whose coordinates are the given points, but with 0.5 subtracted from each coordinate. (POINTL structures are shorthand notation for specifying these fractional coordinate vertices.)




## -see-also




<a href="https://msdn.microsoft.com/fff3df30-cb29-4da3-97bc-dba5fbba1db5">DrvAlphaBlend</a>



<a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/5bd478f1-0c01-4d7f-9ed1-af84e5bbe773">DrvPlgBlt</a>



<a href="https://msdn.microsoft.com/3520533d-4e42-4abc-bc10-557c674caa33">DrvStretchBlt</a>



<a href="https://msdn.microsoft.com/eeaec7f4-2dfe-42a9-8789-a9ce11aec7b2">DrvStretchBltROP</a>



<a href="https://msdn.microsoft.com/67e61a43-b962-4905-8876-9a0380848ed0">DrvTransparentBlt</a>



<a href="https://msdn.microsoft.com/c8839271-0a75-4657-875f-114545f44777">EngAlphaBlend</a>



<a href="https://msdn.microsoft.com/e99dbe54-485b-4a56-9956-2965f04020db">EngBitBlt</a>



<a href="https://msdn.microsoft.com/a25a0fcd-1a61-483a-ba22-1214a9806b70">EngPlgBlt</a>



<a href="https://msdn.microsoft.com/e8f3084c-6216-497b-923a-adef3bfe8bf7">EngStretchBlt</a>



<a href="https://msdn.microsoft.com/db98b15f-6b4b-4efc-aa24-20c728b09358">EngTransparentBlt</a>
 

 

