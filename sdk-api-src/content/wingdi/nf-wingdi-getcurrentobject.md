---
UID: NF:wingdi.GetCurrentObject
title: GetCurrentObject function (wingdi.h)
description: The GetCurrentObject function retrieves a handle to an object of the specified type that has been selected into the specified device context (DC).
helpviewer_keywords: ["GetCurrentObject","GetCurrentObject function [Windows GDI]","OBJ_BITMAP","OBJ_BRUSH","OBJ_COLORSPACE","OBJ_FONT","OBJ_PAL","OBJ_PEN","_win32_GetCurrentObject","gdi.getcurrentobject","wingdi/GetCurrentObject"]
old-location: gdi\getcurrentobject.htm
tech.root: gdi
ms.assetid: d7e2310c-6a9e-4195-824c-1a83382a5c5b
ms.date: 12/05/2018
ms.keywords: GetCurrentObject, GetCurrentObject function [Windows GDI], OBJ_BITMAP, OBJ_BRUSH, OBJ_COLORSPACE, OBJ_FONT, OBJ_PAL, OBJ_PEN, _win32_GetCurrentObject, gdi.getcurrentobject, wingdi/GetCurrentObject
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
 - GetCurrentObject
 - wingdi/GetCurrentObject
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
 - GetCurrentObject
---

# GetCurrentObject function


## -description

The <b>GetCurrentObject</b> function retrieves a handle to an object of the specified type that has been selected into the specified device context (DC).

## -parameters

### -param hdc [in]

A handle to the DC.

### -param type [in]

The object type to be queried. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OBJ_BITMAP"></a><a id="obj_bitmap"></a><dl>
<dt><b>OBJ_BITMAP</b></dt>
</dl>
</td>
<td width="60%">
Returns the current selected bitmap.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJ_BRUSH"></a><a id="obj_brush"></a><dl>
<dt><b>OBJ_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Returns the current selected brush.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJ_COLORSPACE"></a><a id="obj_colorspace"></a><dl>
<dt><b>OBJ_COLORSPACE</b></dt>
</dl>
</td>
<td width="60%">
Returns the current color space.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJ_FONT"></a><a id="obj_font"></a><dl>
<dt><b>OBJ_FONT</b></dt>
</dl>
</td>
<td width="60%">
Returns the current selected font.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJ_PAL"></a><a id="obj_pal"></a><dl>
<dt><b>OBJ_PAL</b></dt>
</dl>
</td>
<td width="60%">
Returns the current selected palette.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJ_PEN"></a><a id="obj_pen"></a><dl>
<dt><b>OBJ_PEN</b></dt>
</dl>
</td>
<td width="60%">
Returns the current selected pen.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a handle to the specified object.

If the function fails, the return value is <b>NULL</b>.

## -remarks

An application can use the <b>GetCurrentObject</b> and <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> functions to retrieve descriptions of the graphic objects currently selected into the specified DC.


#### Examples

For an example, see <a href="/windows/desktop/gdi/retrieving-graphic-object-attributes-and-selecting-new-graphic-objects">Retrieving Graphic-Object Attributes and Selecting New Graphic Objects</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-createcolorspacea">CreateColorSpace</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>