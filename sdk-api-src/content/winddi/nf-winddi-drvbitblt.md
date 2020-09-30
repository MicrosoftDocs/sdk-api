---
UID: NF:winddi.DrvBitBlt
title: DrvBitBlt function (winddi.h)
description: The DrvBitBlt function provides general bit-block transfer capabilities between device-managed surfaces, between GDI-managed standard-format bitmaps, or between a device-managed surface and a GDI-managed standard-format bitmap.
helpviewer_keywords: ["DrvBitBlt","DrvBitBlt function [Display Devices]","ddifncs_1314a0f2-0f0d-4b76-b060-207e332dafde.xml","display.drvbitblt","winddi/DrvBitBlt"]
old-location: display\drvbitblt.htm
tech.root: display
ms.assetid: d7b4e25c-b9a1-4200-b449-b7c7ed059db4
ms.date: 12/05/2018
ms.keywords: DrvBitBlt, DrvBitBlt function [Display Devices], ddifncs_1314a0f2-0f0d-4b76-b060-207e332dafde.xml, display.drvbitblt, winddi/DrvBitBlt
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
 - DrvBitBlt
 - winddi/DrvBitBlt
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
 - DrvBitBlt
---

# DrvBitBlt function


## -description

The <b>DrvBitBlt</b> function provides general bit-block transfer capabilities between <a href="/windows-hardware/drivers/">device-managed surfaces</a>, between GDI-managed standard-format bitmaps, or between a device-managed surface and a GDI-managed standard-format bitmap.

## -parameters

### -param psoTrg [in, out]

Pointer to the <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface on which to draw.

### -param psoSrc [in, optional]

Pointer to a SURFOBJ structure that describes the source for the bit-block transfer operation, if required by the <i>rop4</i> parameter.

### -param psoMask [in, optional]

Pointer to a SURFOBJ structure that describes a surface to be used as a mask for the <i>rop4</i> parameter. The mask is a bitmap with 1 bit per pixel. Typically, a mask is used to limit the area to be modified in the destination surface. Masking is selected by setting the <i>rop4</i> parameter to the value 0xAACC. The destination surface is unaffected if the mask is 0x0000.

The mask will be large enough to cover the destination rectangle.

If this parameter is <b>NULL</b> and a mask is required by the <i>rop4</i> parameter, the implicit mask in the brush is used.

### -param pco [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure that limits the area to be modified. GDI services (<b>CLIPOBJ</b><i>Xxx</i>) that enumerate the <a href="/windows-hardware/drivers/">clip region</a> as a set of rectangles are provided. Whenever possible, GDI simplifies the clipping involved; for example, this function is never called with a single clipping rectangle. GDI clips the destination rectangle before calling this function, making additional clipping unnecessary.

### -param pxlo [in, optional]

Pointer to an <a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a> structure that specifies how color indices should be translated between the source and destination surfaces. If <i>pxlo</i> is <b>NULL</b>, no translation is needed.

If the source surface is palette-managed, its colors are represented by indices into a lookup table of RGB values. The XLATEOBJ structure can be queried for a translate vector that will allow the device driver to translate any source index into a color index for the destination.

The situation is more complicated when, for example, the source is RGB, but the destination is palette-managed. In this case, the closest match to each source RGB value must be found in the destination palette. The driver can call the <a href="/windows/desktop/api/winddi/nf-winddi-xlateobj_ixlate">XLATEOBJ_iXlate</a> service to perform this operation.

Optionally, the device driver can match colors when the target palette is the default device palette.

### -param prclTrg [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that defines the area to be modified. This structure uses the coordinate system of the destination surface. The lower and right edges of this rectangle are not part of the bit-block transfer, meaning the rectangle is lower right exclusive.

<b>DrvBitBlt</b> is never called with an empty destination rectangle. The two points that define the rectangle are always well-ordered. However, on multimonitor systems the rectangle may define a region larger than the destination surface. Drivers should intersect this rectangle with their surface.

### -param pptlSrc [in, optional]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the upper left corner of the source rectangle, if a source exists. This parameter is ignored if there is no source.

### -param pptlMask [in, optional]

Pointer to a POINTL structure that defines which pixel in the mask corresponds to the upper left corner of the source rectangle, if a source exists. This parameter is ignored if the <i>psoMask</i> parameter is <b>NULL</b>.

### -param pbo [in, optional]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a> structure that defines the pattern for the bit-block transfer. GDI's <a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvgetrbrush">BRUSHOBJ_pvGetRbrush</a> service can be used to retrieve the device's realization of the brush. This parameter is ignored if the <i>rop4</i> parameter does not require a pattern.

### -param pptlBrush [in, optional]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure that defines the origin of the brush in the destination surface. The upper left pixel of the brush is aligned at this point, and the brush repeats according to its dimensions. This parameter is ignored if the <i>rop4</i> parameter does not require a pattern.

### -param rop4 [in]

Specifies a raster operation that defines how the mask, pattern, source, and destination pixels are combined to write to the destination surface.

This is a quaternary raster operation, which is an extension of the ternary Rop3 operation. A Rop4 has 16 relevant bits, which are similar to the 8 defining bits of a Rop3. The simplest way to implement a Rop4 is to consider its 2 bytes separately: The low byte specifies a Rop3 that should be calculated if the mask is one, and the high byte specifies a Rop3 that can be calculated and applied if the mask is 0.

## -returns

DrvBitBlt returns <b>TRUE</b> if the bit-block transfer operation is successful. Otherwise, the function returns <b>FALSE</b>, and an error code is logged.

## -remarks

If the driver hooks <b>DrvBitBlt</b>, GDI will call this function when it needs to perform a BitBlt operation where one of the surfaces is a device-managed surface. If the driver implements opaque device-managed bitmaps, it must hook <b>DrvBitBlt</b>; otherwise, hooking <b>DrvBitBlt</b> is optional. If the driver cannot handle the specified call, it may punt the callback to the DIB engine by calling <a href="/windows/desktop/api/winddi/nf-winddi-engbitblt">EngBitBlt</a>.

GDI's <a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a><i>Xxx</i> services allow the clipping to be reduced to a series of clipping rectangles. A translation vector assists in color index translation for palettes.

<div class="alert"><b>Note</b>  Do not dereference parameter pointers unless the <a href="/windows-hardware/drivers/">ROP</a> indicates they are needed. For example, never unnecessarily dereference <i>pbo</i>--&gt;<b>iSolidColor</b> because doing so for a ROP such as BLACKNESS can cause an access violation. (This rule also applies to any function that includes a MIX parameter.)<p class="note">If the driver receives a call to this function in which the <i>rop4</i> parameter is set to 0XCCAA, the driver should punt the call to <a href="/windows/desktop/api/winddi/nf-winddi-engbitblt">EngBitBlt</a>, exposing the device surface(s) as appropriate for the call.

</div>
<div> </div>
For more information about raster operations, see the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-brushobj">BRUSHOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-brushobj_pvgetrbrush">BRUSHOBJ_pvGetRbrush</a>



<a href="/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronize">DrvSynchronize</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engbitblt">EngBitBlt</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatebitmap">EngCreateBitmap</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcreatedevicesurface">EngCreateDeviceSurface</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>



<a href="/windows/desktop/api/winddi/ns-winddi-xlateobj">XLATEOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-xlateobj_ixlate">XLATEOBJ_iXlate</a>