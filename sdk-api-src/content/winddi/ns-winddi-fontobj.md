---
UID: NS:winddi._FONTOBJ
title: FONTOBJ (winddi.h)
description: The FONTOBJ structure is used to give a driver access to information about a particular instance of a font.
helpviewer_keywords: ["FONTOBJ","FONTOBJ structure [Display Devices]","display.fontobj","grstrcts_245faf9a-31c1-4b75-aa97-c4646022cea6.xml","winddi/FONTOBJ"]
old-location: display\fontobj.htm
tech.root: display
ms.assetid: 09af2006-51f1-433e-9227-3c99b9860e75
ms.date: 12/05/2018
ms.keywords: FONTOBJ, FONTOBJ structure [Display Devices], display.fontobj, grstrcts_245faf9a-31c1-4b75-aa97-c4646022cea6.xml, winddi/FONTOBJ
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
req.typenames: FONTOBJ
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FONTOBJ
 - winddi/_FONTOBJ
 - FONTOBJ
 - winddi/FONTOBJ
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
 - FONTOBJ
---

# FONTOBJ structure


## -description

The FONTOBJ structure is used to give a driver access to information about a particular instance of a font.

## -struct-fields

### -field iUniq

Specifies a distinct realization of the font. This value can be used by the driver to identify a GDI font that it might have cached or to identify a driver's realization of its own font. If this member is zero for a GDI font, the font should not be cached.

### -field iFace

Specifies the device index for a device font, which was registered by a call to <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfont">DrvQueryFont</a>. If the font is a GDI font, this member has meaning only to GDI, and the driver should ignore it.

### -field cxMax

Specifies the width, in pixels, of the largest glyph in the specified font.

### -field flFontType

Is a value specifying the type of the font. This member can be a combination of the flags listed in the following table. (Note, however, that FO_GRAY16 and FO_NOGRAY16 are mutually exclusive.)

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
FO_CFF

</td>
<td>
Postscript OpenType font.

</td>
</tr>
<tr>
<td>
FO_DBCS_FONT

</td>
<td>
Font supports DBCS code pages.

</td>
</tr>
<tr>
<td>
FO_EM_HEIGHT

</td>
<td>
TrueType driver internal flag.

</td>
</tr>
<tr>
<td>
FO_GRAY16

</td>
<td>
Font bitmaps are four bits-per-pixel blending (alpha) values.

</td>
</tr>
<tr>
<td>
FO_MULTIPLEMASTER

</td>
<td>
Multiple Master (Type1 or OpenType) font.

</td>
</tr>
<tr>
<td>
FO_NOGRAY16

</td>
<td>
Indicates that the font driver cannot (or will not) grayscale a particular font realization.

</td>
</tr>
<tr>
<td>
FO_POSTSCRIPT

</td>
<td>
Postscript (Type1 or OpenType) font.

</td>
</tr>
<tr>
<td>
FO_SIM_BOLD

</td>
<td>
Driver-simulated bold font.

</td>
</tr>
<tr>
<td>
FO_SIM_ITALIC

</td>
<td>
Driver-simulated italic font.

</td>
</tr>
<tr>
<td>
FO_TYPE_DEVICE

</td>
<td>
Device-specific font.

</td>
</tr>
<tr>
<td>
FO_TYPE_OPENTYPE

</td>
<td>
OpenType font.

</td>
</tr>
<tr>
<td>
FO_TYPE_RASTER

</td>
<td>
Bitmap font.

</td>
</tr>
<tr>
<td>
FO_TYPE_TRUETYPE

</td>
<td>
TrueType font.

</td>
</tr>
<tr>
<td>
FO_VERT_FACE

</td>
<td>
Vertical font.

</td>
</tr>
</table>
 

If the FO_RASTER flag is set, the glyphs written to the specified STROBJ structure are bitmaps, otherwise they are pointers to PATHOBJ structures. If the glyph images are returned in the form of PATHOBJ structures, the driver must inspect the FM_INFO_TECH_STROKE flag of the <b>flInfo</b> member of the associated <a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a> structure. If that flag is set, the paths should be stroked, otherwise the paths must be filled using the alternating mode convention.

If the FO_GRAY16 flag is set, then the font bitmaps are four bits-per-pixel blending (alpha) values. A value of zero means that the resulting pixel should have the same color as the background. If the alpha value is k, then the following table describes the attributes of the resulting pixel, using either linear alpha blending, or gamma-corrected alpha blending. In both methods, the foreground and background colors are, respectively, c<sub>f</sub> and c<sub>b</sub>.

<table>
<tr>
<th>Pixel Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>

<dl>
<dt>Blended Color</dt>
<dt>(linear alpha blending)</dt>
</dl>


</td>
<td>
Linear alpha blending produces a blended color that is a linear combination of the foreground and background colors.

   c = b * c<sub>f</sub> + (1 - b) * c<sub>b</sub>

The blend fraction, b, is obtained as follows:

   b = k / 15, for k = 0, 1, 2, ..., 15

Note: the foreground and background colors include all three color channels (R, G, B).

</td>
</tr>
<tr>
<td>

<dl>
<dt>Blended Color</dt>
<dt>(gamma-corrected alpha blending)</dt>
</dl>


</td>
<td>
Gamma-corrected alpha blending produces a blended color by raising a variable that depends on the alpha value to a fixed power. 

Two formulas are provided: one should be used when the foreground color is numerically larger than the background color; the other should be used in the opposite case. (When the foreground and background colors are equal, both formulas simplify to c = c<sub>b</sub>.) 


<dl>
<dt>If c<sub>f</sub> &gt; c<sub>b</sub>,</dt>
<dt>c = c<sub>b</sub> + <b>pow</b>(b[k], (1 / gamma)) * (c<sub>f</sub> - c<sub>b</sub>)</dt>
</dl>



<dl>
<dt>If c<sub>f</sub> &lt; c<sub>b</sub>,</dt>
<dt>c = c<sub>b</sub> + (1 - <b>pow</b>(1 - b[k], 1 / gamma)) * (c<sub>f</sub> - c<sub>b</sub>)</dt>
</dl>


In these formulas, gamma = 2.33, and b[k] is the k<sup>th</sup> blending fraction, obtained as follows:


<dl>
<dt>   b[k] = 0, for k = 0, and </dt>
<dt>b[k] = (k + 1) / 16, for k = 1, 2, ..., 15</dt>
</dl>


Note: unlike linear alpha blending, these formulas must be applied to <i>each</i> of the three color channels (R, G, B).

</td>
</tr>
</table>
 

GDI sets the FO_GRAY16 flag on entry to the <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfontdata">DrvQueryFontData</a> function when it requests that a font be grayscaled to one of 16 values. If the font driver cannot grayscale a particular font realization, then the font provider clears the FO_GRAY16 flag and sets the FO_NOGRAY16 flag to inform GDI that the grayscaling request will not be satisfied.

### -field iTTUniq

Specifies the associated TrueType file. Two separate point size realizations of a TrueType font face will have FONTOBJ structures that share the same <b>iTTUniq</b> value, but will have different <b>iUniq</b> values. Only TrueType font types can have a nonzero <b>iTTUniq</b> member. For more information see <b>flFontType</b>.

### -field iFile

Pointer to a driver-defined value for device fonts that are already loaded. If the font is a GDI font, then this member is used internally to identify the font and should be ignored.

### -field sizLogResPpi

Specifies the resolution of the device for which this font is realized.

### -field ulStyleSize

Specifies the style size of the font instance, in points.

### -field pvConsumer

Pointer to consumer-allocated data associated with this font instance. A consumer is a driver that accepts glyph information as input for generating text output. Only a font consumer can modify this member. The consumer of this font can store any information in the location pointed to by this member. The engine will not modify this member. The <b>pvConsumer</b> member is guaranteed to be null the first time a FONTOBJ structure is passed to the consumer.

### -field pvProducer

Pointer to producer-allocated data associated with this font instance. A producer is a driver that can produce glyph information as output; this includes glyph metrics, bitmaps, and outlines. Only a font producer can modify this member. The producer of this font can store any information in the location pointed to by this member. The engine will not modify this member. The <b>pvProducer</b> member is guaranteed to be null the first time a FONTOBJ structure is passed to the producer.

## -remarks

As an accelerator, the driver is allowed to access the public members of the FONTOBJ structure.

A driver can be both a producer and a consumer. For example, a printer driver can act as a producer while processing a call to the driver-supplied <a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfontdata">DrvQueryFontData</a> function to provide glyph metrics, and later act a consumer while processing a call to the driver-supplied <a href="/windows/desktop/api/winddi/nf-winddi-drvtextout">DrvTextOut</a> function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvdestroyfont">DrvDestroyFont</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvgetglyphmode">DrvGetGlyphMode</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvqueryfont">DrvQueryFont</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvquerytruetypeoutline">DrvQueryTrueTypeOutline</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_cgetallglyphhandles">FONTOBJ_cGetAllGlyphHandles</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_cgetglyphs">FONTOBJ_cGetGlyphs</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_pifi">FONTOBJ_pifi</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_pxogetxform">FONTOBJ_pxoGetXform</a>



<a href="/windows/desktop/api/winddi/nf-winddi-fontobj_vgetinfo">FONTOBJ_vGetInfo</a>



<a href="/windows/desktop/api/winddi/ns-winddi-ifimetrics">IFIMETRICS</a>