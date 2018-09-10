---
UID: NF:wingdi.CreatePen
title: CreatePen function
author: windows-sdk-content
description: The CreatePen function creates a logical pen that has the specified style, width, and color. The pen can subsequently be selected into a device context and used to draw lines and curves.
old-location: gdi\createpen.htm
tech.root: gdi
ms.assetid: 882facd2-7e06-48f6-82e4-f20e4d5adc92
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreatePen, CreatePen function [Windows GDI], PS_DASH, PS_DASHDOT, PS_DASHDOTDOT, PS_DOT, PS_INSIDEFRAME, PS_NULL, PS_SOLID, _win32_CreatePen, gdi.createpen, wingdi/CreatePen
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

<b>CreatePen</b> returns a pen with the specified width bit with the PS_SOLID style if you specify a width greater than one for the following styles: PS_DASH, PS_DOT, PS_DASHDOT, PS_DASHDOTDOT.


### -param color [in]

A color reference for the pen color. To generate a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value is a handle that identifies a logical pen.

If the function fails, the return value is <b>NULL</b>.




## -remarks



After an application creates a logical pen, it can select that pen into a device context by calling the <a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a> function. After a pen is selected into a device context, it can be used to draw lines and curves.

If the value specified by the <i>nWidth</i> parameter is zero, a line drawn with the created pen always is a single pixel wide regardless of the current transformation.

If the value specified by <i>nWidth</i> is greater than 1, the <i>fnPenStyle</i> parameter must be PS_NULL, PS_SOLID, or PS_INSIDEFRAME.

If the value specified by <i>nWidth</i> is greater than 1 and <i>fnPenStyle</i> is PS_INSIDEFRAME, the line associated with the pen is drawn inside the frame of all primitives except polygons and polylines.

If the value specified by <i>nWidth</i> is greater than 1, <i>fnPenStyle</i> is PS_INSIDEFRAME, and the color specified by the <i>crColor</i> parameter does not match one of the entries in the logical palette, the system draws lines by using a dithered color. Dithered colors are not available with solid pens.

When you no longer need the pen, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

<b>ICM:</b> No color management is done at creation. However, color management is performed when the pen is selected into an ICM-enabled device context.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/2ea32786-f769-4096-8f60-f924c83ca9c8">Creating Colored Pens and Brushes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/638c0294-9a8f-44ed-a791-1be152cd92dd">CreatePenIndirect</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>



<a href="https://msdn.microsoft.com/d5cc81b5-0df4-4ec2-8941-d63819a8d5ff">Pen Functions</a>



<a href="https://msdn.microsoft.com/624c3ea6-6e42-4577-9228-961501633937">Pens Overview</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

