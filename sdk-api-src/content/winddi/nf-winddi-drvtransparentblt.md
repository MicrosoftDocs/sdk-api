---
UID: NF:winddi.DrvTransparentBlt
title: DrvTransparentBlt function
author: windows-sdk-content
description: The DrvTransparentBlt function provides bit-block transfer capabilities with transparency.
old-location: display\drvtransparentblt.htm
tech.root: display
ms.assetid: 67e61a43-b962-4905-8876-9a0380848ed0
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DrvTransparentBlt, DrvTransparentBlt function [Display Devices], ddifncs_962c398c-767b-44de-a1ee-d2b8bf257ec6.xml, display.drvtransparentblt, winddi/DrvTransparentBlt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvTransparentBlt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvTransparentBlt function


## -description


The <b>DrvTransparentBlt</b> function provides bit-block transfer capabilities with transparency.


## -parameters




### -param psoDst [in, out]

Pointer to the <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that identifies the target surface on which to draw.


### -param psoSrc [in]

Pointer to the SURFOBJ structure that identifies the source surface of the bit-block transfer.


### -param pco [in]

Pointer to a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure. The CLIPOBJ_<i>Xxx</i> service routines are provided to enumerate the <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">clip region</a> as a set of rectangles. This enumeration limits the area of the destination that is modified. Whenever possible, GDI simplifies the clipping involved.


### -param pxlo [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure that tells how the source color indices should be translated for writing to the target surface. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.


### -param prclDst [in]

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the rectangular area to be modified. This rectangle is specified in the coordinate system of the destination surface and is defined by two points: upper left and lower right. The rectangle is lower-right exclusive; that is, its lower and right edges are not a part of the bit-block transfer. The two points that define the rectangle are always well ordered.

<b>DrvTransparentBlt</b> is never called with an empty destination rectangle.


### -param prclSrc [in]

Pointer to a RECTL structure that defines the rectangular area to be copied. This rectangle is specified in the coordinate system of the source surface and is defined by two points: upper left and lower right. The two points that define the rectangle are always well ordered.

The source rectangle will never exceed the bounds of the source surface, and so will never overhang the source surface.

This rectangle is mapped to the destination rectangle defined by <i>prclDst</i>. <b>DrvTransparentBlt</b> is never called with an empty source rectangle.


### -param iTransColor [in]

Specifies the physical transparent color in the source surface format. For devices with palettes, this value is a palette index. For devices without palettes, this value is an RGB color in the format that is used in the source surface. For example, if the source surface format is in 5:6:5 RGB form, the value in this parameter will also be in the same form. 


### -param ulReserved [in]

Reserved; this parameter must be set to zero.


## -returns



<b>DrvTransparentBlt</b> returns <b>TRUE</b> upon success. Otherwise, it returns <b>FALSE</b>.




## -remarks



You can optionally implement the <b>DrvTransparentBlt</b> function in graphics drivers.

Bit-block transfer with transparency is supported between two device-managed surfaces or between a device-managed surface and a GDI-managed standard format bitmap. Driver writers are encouraged to support the case of blting from off-screen device bitmaps in video memory to other surfaces in video memory; all other cases can be punted to <a href="https://msdn.microsoft.com/db98b15f-6b4b-4efc-aa24-20c728b09358">EngTransparentBlt</a> with little performance penalty. The driver can punt calls involving device-managed surfaces to <b>EngTransparentBlt</b>.

Any pixels on the source surface that match the transparent color specified by <i>iTransColor</i> are not copied. For a detailed explanation of transparent blts, see <a href="https://msdn.microsoft.com/76e07c66-7e57-42d7-b6da-c13c8e9a8dee">Copying Bitmaps</a>.

The driver will never be called with overlapping source and destination rectangles on the same surface.

The driver should ignore any unused bits in the color key comparison, such as for the most significant bit when the bitmap format is 5:5:5 (five bits each of red, green, and blue).

The driver hooks <b>DrvTransparentBlt</b> by setting the HOOK_TRANSPARENTBLT flag when it calls <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>. If the driver has hooked <b>DrvTransparentBlt</b> and is called to perform an operation that it does not support, the driver should have GDI handle the operation by forwarding the data in a call to <a href="https://msdn.microsoft.com/db98b15f-6b4b-4efc-aa24-20c728b09358">EngTransparentBlt</a>.




## -see-also




<a href="https://msdn.microsoft.com/d7b4e25c-b9a1-4200-b449-b7c7ed059db4">DrvBitBlt</a>



<a href="https://msdn.microsoft.com/5bd478f1-0c01-4d7f-9ed1-af84e5bbe773">DrvPlgBlt</a>



<a href="https://msdn.microsoft.com/3520533d-4e42-4abc-bc10-557c674caa33">DrvStretchBlt</a>



<a href="https://msdn.microsoft.com/eeaec7f4-2dfe-42a9-8789-a9ce11aec7b2">DrvStretchBltROP</a>



<a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>



<a href="https://msdn.microsoft.com/e99dbe54-485b-4a56-9956-2965f04020db">EngBitBlt</a>



<a href="https://msdn.microsoft.com/a25a0fcd-1a61-483a-ba22-1214a9806b70">EngPlgBlt</a>



<a href="https://msdn.microsoft.com/e8f3084c-6216-497b-923a-adef3bfe8bf7">EngStretchBlt</a>



<a href="https://msdn.microsoft.com/d353fab2-ba5d-42a5-8ce7-04fdc731f6ee">EngStretchBltROP</a>



<a href="https://msdn.microsoft.com/db98b15f-6b4b-4efc-aa24-20c728b09358">EngTransparentBlt</a>
 

 

