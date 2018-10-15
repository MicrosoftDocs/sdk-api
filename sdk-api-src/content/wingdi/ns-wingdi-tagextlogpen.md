---
UID: NS:wingdi.tagEXTLOGPEN
title: tagEXTLOGPEN
author: windows-sdk-content
description: The EXTLOGPEN structure defines the pen style, width, and brush attributes for an extended pen.
old-location: gdi\extlogpen.htm
tech.root: gdi
ms.assetid: 34ffa71d-e94d-425e-9f9d-21e3df4990b7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*LPEXTLOGPEN, *NPEXTLOGPEN, *PEXTLOGPEN, EXTLOGPEN, EXTLOGPEN structure [Windows GDI], PEXTLOGPEN, PEXTLOGPEN structure pointer [Windows GDI], _win32_EXTLOGPEN_str, gdi.extlogpen, tagEXTLOGPEN, wingdi/EXTLOGPEN, wingdi/PEXTLOGPEN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - EXTLOGPEN
product: Windows
targetos: Windows
req.typenames: EXTLOGPEN, *PEXTLOGPEN, *NPEXTLOGPEN, *LPEXTLOGPEN
req.redist: 
---

# tagEXTLOGPEN structure


## -description



The <b>EXTLOGPEN</b> structure defines the pen style, width, and brush attributes for an extended pen. This structure is used by the <a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a> function when it retrieves a description of a pen that was created when an application called the <a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a> function.




## -struct-fields




### -field elpPenStyle

A combination of pen type, style, end cap style, and join style. The values from each category can be retrieved by using a bitwise AND operator with the appropriate mask.

The <b>elpPenStyle</b> member masked with PS_TYPE_MASK has one of the following pen type values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PS_GEOMETRIC</td>
<td>The pen is geometric.</td>
</tr>
<tr>
<td>PS_COSMETIC</td>
<td>The pen is cosmetic.</td>
</tr>
</table>
 

The <b>elpPenStyle</b> member masked with PS_STYLE_MASK has one of the following pen styles values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PS_DASH</td>
<td>The pen is dashed.</td>
</tr>
<tr>
<td>PS_DASHDOT</td>
<td>The pen has alternating dashes and dots.</td>
</tr>
<tr>
<td>PS_DASHDOTDOT</td>
<td>The pen has alternating dashes and double dots.</td>
</tr>
<tr>
<td>PS_DOT</td>
<td>The pen is dotted.</td>
</tr>
<tr>
<td>PS_INSIDEFRAME</td>
<td>The pen is solid. When this pen is used in any GDI drawing function that takes a bounding rectangle, the dimensions of the figure are shrunk so that it fits entirely in the bounding rectangle, taking into account the width of the pen. This applies only to PS_GEOMETRIC pens.</td>
</tr>
<tr>
<td>PS_NULL</td>
<td>The pen is invisible.</td>
</tr>
<tr>
<td>PS_SOLID</td>
<td>The pen is solid.</td>
</tr>
<tr>
<td>PS_USERSTYLE</td>
<td>The pen uses a styling array supplied by the user.</td>
</tr>
</table>
 

The following category applies only to PS_GEOMETRIC pens. The <b>elpPenStyle</b> member masked with PS_ENDCAP_MASK has one of the following end cap values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PS_ENDCAP_FLAT</td>
<td>Line end caps are flat.</td>
</tr>
<tr>
<td>PS_ENDCAP_ROUND</td>
<td>Line end caps are round.</td>
</tr>
<tr>
<td>PS_ENDCAP_SQUARE</td>
<td>Line end caps are square.</td>
</tr>
</table>
 

The following category applies only to PS_GEOMETRIC pens. The <b>elpPenStyle</b> member masked with PS_JOIN_MASK has one of the following join values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>PS_JOIN_BEVEL</td>
<td>Line joins are beveled.</td>
</tr>
<tr>
<td>PS_JOIN_MITER</td>
<td>Line joins are mitered when they are within the current limit set by the <a href="https://msdn.microsoft.com/4bed113b-9e3f-441f-96d7-71630bf9298e">SetMiterLimit</a> function. A join is beveled when it would exceed the limit.</td>
</tr>
<tr>
<td>PS_JOIN_ROUND</td>
<td>Line joins are round.</td>
</tr>
</table>
 


### -field elpWidth

The width of the pen. If the <b>elpPenStyle</b> member is PS_GEOMETRIC, this value is the width of the line in logical units. Otherwise, the lines are cosmetic and this value is 1, which indicates a line with a width of one pixel.


### -field elpBrushStyle

The brush style of the pen. The <b>elpBrushStyle</b> member value can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>BS_DIBPATTERN</td>
<td>Specifies a pattern brush defined by a DIB specification. If <b>elpBrushStyle</b> is BS_DIBPATTERN, the <b>elpHatch</b> member contains a handle to a packed DIB. For more information, see discussion in <b>elpHatch</b></td>
</tr>
<tr>
<td>BS_DIBPATTERNPT</td>
<td>Specifies a pattern brush defined by a DIB specification. If <b>elpBrushStyle</b> is BS_DIBPATTERNPT, the <b>elpHatch</b> member contains a pointer to a packed DIB. For more information, see discussion in <b>elpHatch</b>.</td>
</tr>
<tr>
<td>BS_HATCHED</td>
<td>Specifies a hatched brush.</td>
</tr>
<tr>
<td>BS_HOLLOW</td>
<td>Specifies a hollow or <b>NULL</b> brush.</td>
</tr>
<tr>
<td>BS_PATTERN</td>
<td>Specifies a pattern brush defined by a memory bitmap.</td>
</tr>
<tr>
<td>BS_SOLID</td>
<td>Specifies a solid brush.</td>
</tr>
</table>
 


### -field elpColor

If <b>elpBrushStyle</b> is BS_SOLID or BS_HATCHED, <b>elpColor</b> specifies the color in which the pen is to be drawn. For BS_HATCHED, the <a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a> and <a href="https://msdn.microsoft.com/9163370b-19c5-4c23-9197-793e4b8d50c4">SetBkColor</a> functions determine the background color.

If <b>elpBrushStyle</b> is BS_HOLLOW or BS_PATTERN, <b>elpColor</b> is ignored.

If <b>elpBrushStyle</b> is BS_DIBPATTERN or BS_DIBPATTERNPT, the low-order word of <b>elpColor</b> specifies whether the <b>bmiColors</b> member of the <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure contain explicit RGB values or indices into the currently realized logical palette. The <b>elpColor</b> value must be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DIB_PAL_COLORS</td>
<td>The color table consists of an array of 16-bit indices into the currently realized logical palette.</td>
</tr>
<tr>
<td>DIB_RGB_COLORS</td>
<td>The color table contains literal RGB values.</td>
</tr>
</table>
 

The <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro is used to generate a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure.


### -field elpHatch

If <b>elpBrushStyle</b> is BS_PATTERN, <b>elpHatch</b> is a handle to the bitmap that defines the pattern.

If <b>elpBrushStyle</b> is BS_SOLID or BS_HOLLOW, <b>elpHatch</b> is ignored.

If <b>elpBrushStyle</b> is BS_DIBPATTERN, the <b>elpHatch</b> member is a handle to a packed DIB. To obtain this handle, an application calls the <a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> function with GMEM_MOVEABLE (or <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> with LMEM_MOVEABLE) to allocate a block of memory and then fills the memory with the packed DIB. A packed DIB consists of a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure immediately followed by the array of bytes that define the pixels of the bitmap.

If <b>elpBrushStyle</b> is BS_DIBPATTERNPT, the <b>elpHatch</b> member is a pointer to a packed DIB. The pointer derives from the memory block created by <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> with LMEM_FIXED set or by <a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> with GMEM_FIXED set, or it is the pointer returned by a call like <a href="https://msdn.microsoft.com/a9432e28-9fbd-4a7e-8dce-fad3da04804a">LocalLock</a> (handle_to_the_dib). A packed DIB consists of a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure immediately followed by the array of bytes that define the pixels of the bitmap.

If <b>elpBrushStyle</b> is BS_HATCHED, the <b>elpHatch</b> member specifies the orientation of the lines used to create the hatch. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>HS_BDIAGONAL</td>
<td>45-degree upward hatch (left to right)</td>
</tr>
<tr>
<td>HS_CROSS</td>
<td>Horizontal and vertical crosshatch</td>
</tr>
<tr>
<td>HS_DIAGCROSS</td>
<td>45-degree crosshatch</td>
</tr>
<tr>
<td>HS_FDIAGONAL</td>
<td>45-degree downward hatch (left to right)</td>
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
 


### -field elpNumEntries

The number of entries in the style array in the <b>elpStyleEntry</b> member. This value is zero if <b>elpPenStyle</b> does not specify PS_USERSTYLE.


### -field elpStyleEntry

A user-supplied style array. The array is specified with a finite length, but it is used as if it repeated indefinitely. The first entry in the array specifies the length of the first dash. The second entry specifies the length of the first gap. Thereafter, lengths of dashes and gaps alternate.

If <b>elpWidth</b> specifies geometric lines, the lengths are in logical units. Otherwise, the lines are cosmetic and lengths are in device units.


## -see-also




<a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/dcc65b2d-958a-4681-962f-a94895f0f243">Pen Structures</a>



<a href="https://msdn.microsoft.com/624c3ea6-6e42-4577-9228-961501633937">Pens Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/9163370b-19c5-4c23-9197-793e4b8d50c4">SetBkColor</a>



<a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a>
 

 

