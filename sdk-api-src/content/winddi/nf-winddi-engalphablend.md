---
UID: NF:winddi.EngAlphaBlend
title: EngAlphaBlend function
author: windows-sdk-content
description: The EngAlphaBlend function provides bit-block transfer capabilities with alpha blending.
old-location: display\engalphablend.htm
tech.root: display
ms.assetid: c8839271-0a75-4657-875f-114545f44777
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EngAlphaBlend, EngAlphaBlend function [Display Devices], display.engalphablend, gdifncs_f7f6d10b-db7e-40af-8378-05cca946505f.xml, winddi/EngAlphaBlend
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
 - EngAlphaBlend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngAlphaBlend function


## -description


The <b>EngAlphaBlend</b> function provides bit-block transfer capabilities with <a href="https://msdn.microsoft.com/4ef14b5b-128b-4b7c-9211-116e8bd60cab">alpha blending</a>.


## -parameters




### -param psoDest

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that identifies the surface on which to draw.


### -param psoSrc

Pointer to a SURFOBJ structure that identifies the source surface.


### -param pco

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. The <b>CLIPOBJ_</b><b><i>Xxx</i></b> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles. This enumeration limits the area of the destination that is modified. Whenever possible, GDI simplifies the clipping involved. However, unlike <a href="https://msdn.microsoft.com/e99dbe54-485b-4a56-9956-2965f04020db">EngBitBlt</a>, <b>EngAlphaBlend</b> might be called with a single rectangle in order to prevent round-off errors in clipping the output.


### -param pxlo

Pointer to a <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure that specifies how color indices should be translated between the source and destination surfaces.

If the source surface is palette managed, its colors are represented by indices into a lookup table of RGB color values. In this case, GDI can query the XLATEOBJ structure for a translate vector to quickly translate any source index into a color index for the destination.

The situation is more complicated when, for example, the source is RGB but the destination is palette-managed. In this case, the closest match to each source RGB value must be found in the destination palette. GDI calls the <a href="https://msdn.microsoft.com/1506efcb-d4fa-4120-89ba-5aca0f3c7f97">XLATEOBJ_iXlate</a> service routine to perform this matching operation.


### -param prclDest

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the rectangular area to be modified. This rectangle is specified in the coordinate system of the destination surface and is defined by two points: upper left and lower right. The two points that define the rectangle are always well ordered.

The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the blend.

The specified rectangle can overhang the destination surface; GDI performs the proper clipping when it does.

<b>EngAlphaBlend</b> must never be called with an empty destination rectangle.


### -param prclSrc

Pointer to a RECTL structure that defines the area to be copied. This rectangle is specified in the coordinate system of the source surface and is defined by two points: upper left and lower right. The two points that define the rectangle are always well ordered.

The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the blend.

The source rectangle must never exceed the bounds of the source surface, and thus never overhang the source surface.

<b>EngAlphaBlend</b> must never be called with an empty source rectangle.

The mapping is defined by <i>prclSrc</i> and <i>prclDest</i>. The points specified in <i>prclDest</i> and <i>prclSrc</i> lie on integer coordinates, which correspond to pixel centers. A rectangle defined by two such points is considered to be a geometric rectangle with two vertices whose coordinates are the given points, but with 0.5 subtracted from each coordinate. (POINTL structures are shorthand notation for specifying these fractional coordinate vertices.)


### -param pBlendObj

Pointer to a <a href="https://msdn.microsoft.com/1bbe5cb6-8722-45bb-ae43-01bc4460f08d">BLENDOBJ</a> structure that describes the blending operation to perform between the source and destination surfaces. This structure is a wrapper for the BLENDFUNCTION structure, which includes necessary source and destination format information that is not available in the XLATEOBJ structure . BLENDFUNCTION is declared in the Microsoft Windows SDK documentation. Its members are defined as follows:

<b>BlendOp</b> defines the blend operation to be performed. Currently this value must be AC_SRC_OVER, which means that the source bitmap is placed over the destination bitmap based on the alpha values of the source pixels. There are three possible cases that this blend operation should handle. These are described in the Remarks section of this reference page.

<b>BlendFlags</b> is reserved and is currently set to zero.

<b>SourceConstantAlpha</b> defines the constant blend factor to apply to the entire source surface. This value is in the range of [0,255], where 0 is completely transparent and 255 is completely opaque.

<b>AlphaFormat</b> defines whether the surface is assumed to have an alpha channel. This member can optionally be set to the following value:





#### AC_SRC_ALPHA

The source surface can be assumed to be in a premultiplied alpha 32bpp "BGRA" format; that is, the surface type is BMF_32BPP and the palette type is BI_RGB. The alpha component is an integer in the range of [0,255], where 0 is completely transparent and 255 is completely opaque.


## -returns



<b>EngAlphaBlend</b> returns <b>TRUE</b> upon success. If an error occurs, it returns <b>FALSE</b> and reports an error code.




## -remarks



A bit-block transfer with alpha blending is supported between the following surfaces:

<ul>
<li>
From one <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device-managed surface</a> to another device-managed surface.

</li>
<li>
From one GDI-managed standard format bitmap to another GDI-managed standard format bitmap.

</li>
<li>
From one device-managed surface to a GDI-managed surface, and vice versa.

</li>
</ul>
The driver should never call <b>EngAlphaBlend</b> with overlapping source and destination rectangles on the same surface.

The three possible cases for the AC_SRC_OVER blend function are:

<ul>
<li>The source bitmap has no per-pixel alpha (AC_SRC_ALPHA is not set), so the blend is applied to the pixel's color channels based on the constant source alpha value specified in <b>SourceConstantAlpha</b> as follows:

<div class="code"><span codelanguage=""><table>
<li>The source bitmap has no per-pixel alpha (AC_SRC_ALPHA is not set), so the blend is applied to the pixel's color channels based on the constant source alpha value specified in <b>SourceConstantAlpha</b> as follows:<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Dst.Red = Round(((Src.Red * SourceConstantAlpha) + 
    ((255 − SourceConstantAlpha) * Dst.Red)) / 255);
Dst.Green = Round(((Src.Green * SourceConstantAlpha) + 
    ((255 − SourceConstantAlpha) * Dst.Green)) / 255);
Dst.Blue = Round(((Src.Blue * SourceConstantAlpha) + 
    ((255 − SourceConstantAlpha) * Dst.Blue)) / 255);
/* Do the next computation only if the destination bitmap 
    has an alpha channel. */
Dst.Alpha = Round(((Src.Alpha * SourceConstantAlpha) + 
    ((255 − SourceConstantAlpha) * Dst.Alpha)) / 255);</pre>
</td>
</tr>
</table></span></div>


</li>
<li>The source bitmap has per-pixel alpha values (AC_SRC_ALPHA is set), and <b>SourceConstantAlpha</b> is not used (it is set to 255). The blend is computed as follows:

<div class="code"><span codelanguage=""><table>
<li>The source bitmap has per-pixel alpha values (AC_SRC_ALPHA is set), and <b>SourceConstantAlpha</b> is not used (it is set to 255). The blend is computed as follows:<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Dst.Red = Src.Red + 
    Round(((255 − Src.Alpha) * Dst.Red) / 255);
Dst.Green = Src.Green + 
    Round(((255 − Src.Alpha) * Dst.Green) / 255);
Dst.Blue = Src.Blue + 
    Round(((255 − Src.Alpha) * Dst.Blue) / 255);
/* Do the next computation only if the destination bitmap 
    has an alpha channel. */
Dst.Alpha = Src.Alpha + 
    Round(((255 − Src.Alpha) * Dst.Alpha) / 255);</pre>
</td>
</tr>
</table></span></div>


</li>
<li>The source bitmap has per-pixel alpha values (AC_SRC_ALPHA is set), and <b>SourceConstantAlpha</b> is used (it is not set to 255). The blend is computed as follows:

<div class="code"><span codelanguage=""><table>
<li>The source bitmap has per-pixel alpha values (AC_SRC_ALPHA is set), and <b>SourceConstantAlpha</b> is used (it is not set to 255). The blend is computed as follows:<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Temp.Red = Round((Src.Red * SourceConstantAlpha) / 255);
Temp.Green = Round((Src.Green * SourceConstantAlpha) / 255);
Temp.Blue = Round((Src.Blue * SourceConstantAlpha) / 255);
/* The next computation must be done even if the 
    destination bitmap does not have an alpha channel. */
Temp.Alpha = Round((Src.Alpha * SourceConstantAlpha) / 255);
 
/* Note that the following equations use the just-computed 
   Temp.Alpha value: */
Dst.Red = Temp.Red + 
    Round(((255 − Temp.Alpha) * Dst.Red) / 255);
Dst.Green = Temp.Green + 
    Round(((255 − Temp.Alpha) * Dst.Green) / 255);
Dst.Blue = Temp.Blue + 
    Round(((255 − Temp.Alpha) * Dst.Blue) / 255);
/* Do the next computation only if the destination bitmap 
    has an alpha channel. */
Dst.Alpha = Temp.Alpha + 
    Round(((255 − Temp.Alpha) * Dst.Alpha) / 255);</pre>
</td>
</tr>
</table></span></div>


</li>
</ul>
The driver should call <b>EngAlphaBlend</b> if it has hooked <a href="https://msdn.microsoft.com/fff3df30-cb29-4da3-97bc-dba5fbba1db5">DrvAlphaBlend</a> and it is called to do something that it does not support.




## -see-also




<a href="https://msdn.microsoft.com/fff3df30-cb29-4da3-97bc-dba5fbba1db5">DrvAlphaBlend</a>



<a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/5bd478f1-0c01-4d7f-9ed1-af84e5bbe773">DrvPlgBlt</a>



<a href="https://msdn.microsoft.com/3520533d-4e42-4abc-bc10-557c674caa33">DrvStretchBlt</a>



<a href="https://msdn.microsoft.com/eeaec7f4-2dfe-42a9-8789-a9ce11aec7b2">DrvStretchBltROP</a>



<a href="https://msdn.microsoft.com/67e61a43-b962-4905-8876-9a0380848ed0">DrvTransparentBlt</a>



<a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>



<a href="https://msdn.microsoft.com/e99dbe54-485b-4a56-9956-2965f04020db">EngBitBlt</a>



<a href="https://msdn.microsoft.com/a25a0fcd-1a61-483a-ba22-1214a9806b70">EngPlgBlt</a>



<a href="https://msdn.microsoft.com/e8f3084c-6216-497b-923a-adef3bfe8bf7">EngStretchBlt</a>



<a href="https://msdn.microsoft.com/d353fab2-ba5d-42a5-8ce7-04fdc731f6ee">EngStretchBltROP</a>



<a href="https://msdn.microsoft.com/db98b15f-6b4b-4efc-aa24-20c728b09358">EngTransparentBlt</a>
 

 

