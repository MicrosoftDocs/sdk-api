---
UID: NF:wingdi.CreatePen
title: CreatePen function (wingdi.h)
description: The CreatePen function creates a logical pen that has the specified style, width, and color. The pen can subsequently be selected into a device context and used to draw lines and curves.
helpviewer_keywords: ["CreatePen","CreatePen function [Windows GDI]","PS_DASH","PS_DASHDOT","PS_DASHDOTDOT","PS_DOT","PS_INSIDEFRAME","PS_NULL","PS_SOLID","_win32_CreatePen","gdi.createpen","wingdi/CreatePen"]
old-location: gdi\createpen.htm
tech.root: gdi
ms.assetid: 882facd2-7e06-48f6-82e4-f20e4d5adc92
ms.date: 12/05/2018
ms.keywords: CreatePen, CreatePen function [Windows GDI], PS_DASH, PS_DASHDOT, PS_DASHDOTDOT, PS_DOT, PS_INSIDEFRAME, PS_NULL, PS_SOLID, _win32_CreatePen, gdi.createpen, wingdi/CreatePen
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreatePen
 - wingdi/CreatePen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - CreatePen
---

# CreatePen function


## -description

The <b>CreatePen</b> function creates a logical pen that has the specified style, width, and color. The pen can subsequently be selected into a device context and used to draw lines and curves.

## -parameters

### -param iStyle [in]

The pen style. It can be any one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PS_SOLID"></a><a id="ps_solid"></a><dl>
<dt><b>PS_SOLID</b></dt>
</dl>
</td>
<td width="60%">
The pen is solid.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DASH"></a><a id="ps_dash"></a><dl>
<dt><b>PS_DASH</b></dt>
</dl>
</td>
<td width="60%">
The pen is dashed. This style is valid only when the pen width is one or less in device units.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DOT"></a><a id="ps_dot"></a><dl>
<dt><b>PS_DOT</b></dt>
</dl>
</td>
<td width="60%">
The pen is dotted. This style is valid only when the pen width is one or less in device units.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DASHDOT"></a><a id="ps_dashdot"></a><dl>
<dt><b>PS_DASHDOT</b></dt>
</dl>
</td>
<td width="60%">
The pen has alternating dashes and dots. This style is valid only when the pen width is one or less in device units.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_DASHDOTDOT"></a><a id="ps_dashdotdot"></a><dl>
<dt><b>PS_DASHDOTDOT</b></dt>
</dl>
</td>
<td width="60%">
The pen has alternating dashes and double dots. This style is valid only when the pen width is one or less in device units.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_NULL"></a><a id="ps_null"></a><dl>
<dt><b>PS_NULL</b></dt>
</dl>
</td>
<td width="60%">
The pen is invisible.

</td>
</tr>
<tr>
<td width="40%"><a id="PS_INSIDEFRAME"></a><a id="ps_insideframe"></a><dl>
<dt><b>PS_INSIDEFRAME</b></dt>
</dl>
</td>
<td width="60%">
The pen is solid. When this pen is used in any GDI drawing function that takes a bounding rectangle, the dimensions of the figure are shrunk so that it fits entirely in the bounding rectangle, taking into account the width of the pen. This applies only to geometric pens.

</td>
</tr>
</table>

### -param cWidth [in]

The width of the pen, in logical units. If <i>nWidth</i> is zero, the pen is a single pixel wide, regardless of the current transformation.

<b>CreatePen</b> returns a pen with the specified width but with the PS_SOLID style if you specify a width greater than one for the following styles: PS_DASH, PS_DOT, PS_DASHDOT, PS_DASHDOTDOT.

### -param color [in]

A color reference for the pen color. To generate a <a href="/windows/desktop/gdi/colorref">COLORREF</a> structure, use the <a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.

## -returns

If the function succeeds, the return value is a handle that identifies a logical pen.

If the function fails, the return value is <b>NULL</b>.

## -remarks

After an application creates a logical pen, it can select that pen into a device context by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a> function. After a pen is selected into a device context, it can be used to draw lines and curves.

If the value specified by the <i>nWidth</i> parameter is zero, a line drawn with the created pen always is a single pixel wide regardless of the current transformation.

If the value specified by <i>nWidth</i> is greater than 1, the <i>fnPenStyle</i> parameter must be PS_NULL, PS_SOLID, or PS_INSIDEFRAME.

If the value specified by <i>nWidth</i> is greater than 1 and <i>fnPenStyle</i> is PS_INSIDEFRAME, the line associated with the pen is drawn inside the frame of all primitives except polygons and polylines.

If the value specified by <i>nWidth</i> is greater than 1, <i>fnPenStyle</i> is PS_INSIDEFRAME, and the color specified by the <i>crColor</i> parameter does not match one of the entries in the logical palette, the system draws lines by using a dithered color. Dithered colors are not available with solid pens.

When using an <i>iStyle</i> parameter of PS_DASH, PS_DOT, PS_DASHDOT or PS_DASHDOTDOT, in order to make the gaps between the dashes or dots transparent, use <a href="/windows/win32/api/wingdi/nf-wingdi-setbkmode">SetBkMode</a> to set the mode to TRANSPARENT.

When you no longer need the pen, call the <a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

<b>ICM:</b> No color management is done at creation. However, color management is performed when the pen is selected into an ICM-enabled device context.


#### Examples

For an example, see <a href="/windows/desktop/gdi/creating-colored-pens-and-brushes">Creating Colored Pens and Brushes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpenindirect">CreatePenIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>



<a href="/windows/desktop/gdi/pen-functions">Pen Functions</a>



<a href="/windows/desktop/gdi/pens">Pens Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>
