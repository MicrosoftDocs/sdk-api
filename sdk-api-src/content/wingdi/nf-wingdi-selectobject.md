---
UID: NF:wingdi.SelectObject
title: SelectObject function (wingdi.h)
description: The SelectObject function selects an object into the specified device context (DC). The new object replaces the previous object of the same type.
helpviewer_keywords: ["Bitmap","Brush","Font","Pen","Region","SelectObject","SelectObject function [Windows GDI]","_win32_SelectObject","gdi.selectobject","wingdi/SelectObject"]
old-location: gdi\selectobject.htm
tech.root: gdi
ms.assetid: a89b875e-923d-4048-bc61-8dea132cc56d
ms.date: 12/05/2018
ms.keywords: Bitmap, Brush, Font, Pen, Region, SelectObject, SelectObject function [Windows GDI], _win32_SelectObject, gdi.selectobject, wingdi/SelectObject
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
 - SelectObject
 - wingdi/SelectObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - SelectObject
---

# SelectObject function


## -description

The <b>SelectObject</b> function selects an object into the specified device context (DC). The new object replaces the previous object of the same type.

## -parameters

### -param hdc [in]

A handle to the DC.

### -param h [in]

A handle to the object to be selected. The specified object must have been created by using one of the following functions.

<table>
<tr>
<th>Object</th>
<th>Functions</th>
</tr>
<tr>
<td width="40%"><a id="Bitmap"></a><a id="bitmap"></a><a id="BITMAP"></a><dl>
<dt><b>Bitmap</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmap">CreateBitmap</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmapindirect">CreateBitmapIndirect</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>


Bitmaps can only be selected into memory DC's. A single bitmap cannot be selected into more than one DC at the same time.

</td>
</tr>
<tr>
<td width="40%"><a id="Brush"></a><a id="brush"></a><a id="BRUSH"></a><dl>
<dt><b>Brush</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect">CreateBrushIndirect</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrushpt">CreateDIBPatternBrushPt</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>


</td>
</tr>
<tr>
<td width="40%"><a id="Font"></a><a id="font"></a><a id="FONT"></a><dl>
<dt><b>Font</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>


</td>
</tr>
<tr>
<td width="40%"><a id="Pen"></a><a id="pen"></a><a id="PEN"></a><dl>
<dt><b>Pen</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createpenindirect">CreatePenIndirect</a>


</td>
</tr>
<tr>
<td width="40%"><a id="Region"></a><a id="region"></a><a id="REGION"></a><dl>
<dt><b>Region</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/wingdi/nf-wingdi-combinergn">CombineRgn</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgn">CreateEllipticRgn</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgnindirect">CreateEllipticRgnIndirect</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>, <a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>


</td>
</tr>
</table>

## -returns

If the selected object is not a region and the function succeeds, the return value is a handle to the object being replaced. If the selected object is a region and the function succeeds, the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>Region consists of a single rectangle.</td>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>Region consists of more than one rectangle.</td>
</tr>
<tr>
<td>NULLREGION</td>
<td>Region is empty.</td>
</tr>
</table>
 

If an error occurs and the selected object is not a region, the return value is <b>NULL</b>. Otherwise, it is HGDI_ERROR.

## -remarks

This function returns the previously selected object of the specified type. An application should always replace a new object with the original, default object after it has finished drawing with the new object.

An application cannot select a single bitmap into more than one DC at a time.

<b>ICM:</b> If the object being selected is a brush or a pen, color management is performed.


#### Examples

For an example, see <a href="/windows/desktop/gdi/setting-the-pen-or-brush-color">Setting the Pen or Brush Color</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-combinergn">CombineRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmap">CreateBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbitmapindirect">CreateBitmapIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect">CreateBrushIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createcompatiblebitmap">CreateCompatibleBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibpatternbrush">CreateDIBPatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibitmap">CreateDIBitmap</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgn">CreateEllipticRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createellipticrgnindirect">CreateEllipticRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createfonta">CreateFont</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createfontindirecta">CreateFontIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createhatchbrush">CreateHatchBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpatternbrush">CreatePatternBrush</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpen">CreatePen</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpenindirect">CreatePenIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createrectrgnindirect">CreateRectRgnIndirect</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush">CreateSolidBrush</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectpalette">SelectPalette</a>