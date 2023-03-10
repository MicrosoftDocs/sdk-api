---
UID: NS:wingdi.tagLOGBRUSH32
title: LOGBRUSH32 (wingdi.h)
description: The LOGBRUSH32 structure defines the style, color, and pattern of a physical brush.
helpviewer_keywords: ["*LPLOGBRUSH32","*NPLOGBRUSH32","*PLOGBRUSH32","LOGBRUSH32","LOGBRUSH32 structure [Windows GDI]","PLOGBRUSH32","PLOGBRUSH32 structure pointer [Windows GDI]","_win32_LOGBRUSH32_str","gdi.logbrush32","wingdi/LOGBRUSH32","wingdi/PLOGBRUSH32"]
old-location: gdi\logbrush32.htm
tech.root: gdi
ms.assetid: 8e2053a9-d7b6-4bf7-b915-4c3871a46b37
ms.date: 12/05/2018
ms.keywords: '*LPLOGBRUSH32, *NPLOGBRUSH32, *PLOGBRUSH32, LOGBRUSH32, LOGBRUSH32 structure [Windows GDI], PLOGBRUSH32, PLOGBRUSH32 structure pointer [Windows GDI], _win32_LOGBRUSH32_str, gdi.logbrush32, wingdi/LOGBRUSH32, wingdi/PLOGBRUSH32'
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: LOGBRUSH32, *PLOGBRUSH32, *NPLOGBRUSH32, *LPLOGBRUSH32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLOGBRUSH32
 - wingdi/tagLOGBRUSH32
 - PLOGBRUSH32
 - wingdi/PLOGBRUSH32
 - LOGBRUSH32
 - wingdi/LOGBRUSH32
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - LOGBRUSH32
---

# LOGBRUSH32 structure


## -description

The <b>LOGBRUSH32</b> structure defines the style, color, and pattern of a physical brush. It is similar to <a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>, but it is used to maintain compatibility between 32-bit platforms and 64-bit platforms when we record the metafile record on one platform and then play it on another. Thus, it is only used in <a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatebrushindirect">EMRCREATEBRUSHINDIRECT</a>. If the code will only be on one platform, <b>LOGBRUSH</b> is sufficient.

## -struct-fields

### -field lbStyle

The brush style. The <b>lbStyle</b> member must be one of the following styles.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>BS_DIBPATTERN</td>
<td>A pattern brush defined by a device-independent bitmap (DIB) specification. If <b>lbStyle</b> is BS_DIBPATTERN, the <b>lbHatch</b> member contains a handle to a packed DIB. For more information, see discussion in <b>lbHatch</b>.</td>
</tr>
<tr>
<td>BS_DIBPATTERN8X8</td>
<td>Same as BS_DIBPATTERN.</td>
</tr>
<tr>
<td>BS_DIBPATTERNPT</td>
<td>A pattern brush defined by a device-independent bitmap (DIB) specification. If <b>lbStyle</b> is BS_DIBPATTERNPT, the <b>lbHatch</b> member contains a pointer to a packed DIB. For more information, see discussion in <b>lbHatch</b>.</td>
</tr>
<tr>
<td>BS_HATCHED</td>
<td>Hatched brush.</td>
</tr>
<tr>
<td>BS_HOLLOW</td>
<td>Hollow brush.</td>
</tr>
<tr>
<td>BS_NULL</td>
<td>Same as BS_HOLLOW.</td>
</tr>
<tr>
<td>BS_PATTERN</td>
<td>Pattern brush defined by a memory bitmap.</td>
</tr>
<tr>
<td>BS_PATTERN8X8</td>
<td>Same as BS_PATTERN.</td>
</tr>
<tr>
<td>BS_SOLID</td>
<td>Solid brush.</td>
</tr>
</table>

### -field lbColor

The color in which the brush is to be drawn. If <b>lbStyle</b> is the BS_HOLLOW or BS_PATTERN style, <b>lbColor</b> is ignored.

If <b>lbStyle</b> is BS_DIBPATTERN or BS_DIBPATTERNPT, the low-order word of <b>lbColor</b> specifies whether the <b>bmiColors</b> members of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure contain explicit red, green, blue (RGB) values or indexes into the currently realized logical palette. The <b>lbColor</b> member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DIB_PAL_COLORS</td>
<td>The color table consists of an array of 16-bit indexes into the currently realized logical palette.</td>
</tr>
<tr>
<td>DIB_RGB_COLORS</td>
<td>The color table contains literal RGB values.</td>
</tr>
</table>
 

If <b>lbStyle</b> is BS_HATCHED or BS_SOLID, <b>lbColor</b> is a <a href="/windows/desktop/gdi/colorref">COLORREF</a> color value. To create a <b>COLORREF</b> color value, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

### -field lbHatch

A hatch style. The meaning depends on the brush style defined by <b>lbStyle</b>.

If <b>lbStyle</b> is BS_DIBPATTERN, the <b>lbHatch</b> member contains a handle to a packed DIB. To obtain this handle, an application calls the <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> function with GMEM_MOVEABLE (or <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> with LMEM_MOVEABLE) to allocate a block of memory and then fills the memory with the packed DIB. A packed DIB consists of a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure immediately followed by the array of bytes that define the pixels of the bitmap.

If <b>lbStyle</b> is BS_DIBPATTERNPT, the <b>lbHatch</b> member contains a pointer to a packed DIB. The pointer derives from the memory block created by <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> with LMEM_FIXED set or by <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> with GMEM_FIXED set, or it is the pointer returned by a call like <a href="/windows/desktop/api/winbase/nf-winbase-locallock">LocalLock</a> (handle_to_the_dib). A packed DIB consists of a <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a> structure immediately followed by the array of bytes that define the pixels of the bitmap.

If <b>lbStyle</b> is BS_HATCHED, the <b>lbHatch</b> member specifies the orientation of the lines used to create the hatch. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>HS_BDIAGONAL</td>
<td>A 45-degree upward, left-to-right hatch</td>
</tr>
<tr>
<td>HS_CROSS</td>
<td>Horizontal and vertical cross-hatch</td>
</tr>
<tr>
<td>HS_DIAGCROSS</td>
<td>45-degree crosshatch</td>
</tr>
<tr>
<td>HS_FDIAGONAL</td>
<td>A 45-degree downward, left-to-right hatch</td>
</tr>
<tr>
<td>HS_HORIZONTAL</td>
<td>Horizontal hatch</td>
</tr>
<tr>
<td>HS_VERTICAL</td>
<td>Vertical hatch</td>
</tr>
</table>
 

If <b>lbStyle</b> is BS_PATTERN, <b>lbHatch</b> is a handle to the bitmap that defines the pattern. The bitmap cannot be a DIB section bitmap, which is created by the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a> function.

If <b>lbStyle</b> is BS_SOLID or BS_HOLLOW, <b>lbHatch</b> is ignored.

## -remarks

Although <b>lbColor</b> controls the foreground color of a hatch brush, the <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkmode">SetBkMode</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a> functions control the background color.

Brushes can be created from bitmaps or DIBs larger than 8 by 8 pixels.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfo">BITMAPINFO</a>



<a href="/windows/desktop/gdi/brush-structures">Brush Structures</a>



<a href="/windows/desktop/gdi/brushes">Brushes Overview</a>



<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-emrcreatebrushindirect">EMRCREATEBRUSHINDIRECT</a>



<a href="/windows/desktop/api/wingdi/ns-wingdi-logbrush">LOGBRUSH</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkmode">SetBkMode</a>