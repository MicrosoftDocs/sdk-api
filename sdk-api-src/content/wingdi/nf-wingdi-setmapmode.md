---
UID: NF:wingdi.SetMapMode
title: SetMapMode function (wingdi.h)
description: The SetMapMode function sets the mapping mode of the specified device context. The mapping mode defines the unit of measure used to transform page-space units into device-space units, and also defines the orientation of the device's x and y axes.
helpviewer_keywords: ["MM_ANISOTROPIC","MM_HIENGLISH","MM_HIMETRIC","MM_ISOTROPIC","MM_LOENGLISH","MM_LOMETRIC","MM_TEXT","MM_TWIPS","SetMapMode","SetMapMode function [Windows GDI]","_win32_SetMapMode","gdi.setmapmode","wingdi/SetMapMode"]
old-location: gdi\setmapmode.htm
tech.root: gdi
ms.assetid: a4d6a63a-6d2d-4bd9-9e71-4cd1b5f145a4
ms.date: 12/05/2018
ms.keywords: MM_ANISOTROPIC, MM_HIENGLISH, MM_HIMETRIC, MM_ISOTROPIC, MM_LOENGLISH, MM_LOMETRIC, MM_TEXT, MM_TWIPS, SetMapMode, SetMapMode function [Windows GDI], _win32_SetMapMode, gdi.setmapmode, wingdi/SetMapMode
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
 - SetMapMode
 - wingdi/SetMapMode
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
 - SetMapMode
---

# SetMapMode function


## -description

The <b>SetMapMode</b> function sets the mapping mode of the specified device context. The mapping mode defines the unit of measure used to transform page-space units into device-space units, and also defines the orientation of the device's x and y axes.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param iMode [in]

The new mapping mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MM_ANISOTROPIC"></a><a id="mm_anisotropic"></a><dl>
<dt><b>MM_ANISOTROPIC</b></dt>
</dl>
</td>
<td width="60%">
Logical units are mapped to arbitrary units with arbitrarily scaled axes. Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a> functions to specify the units, orientation, and scaling.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_HIENGLISH"></a><a id="mm_hienglish"></a><dl>
<dt><b>MM_HIENGLISH</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.001 inch. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_HIMETRIC"></a><a id="mm_himetric"></a><dl>
<dt><b>MM_HIMETRIC</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.01 millimeter. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_ISOTROPIC"></a><a id="mm_isotropic"></a><dl>
<dt><b>MM_ISOTROPIC</b></dt>
</dl>
</td>
<td width="60%">
Logical units are mapped to arbitrary units with equally scaled axes; that is, one unit along the x-axis is equal to one unit along the y-axis. Use the <a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a> functions to specify the units and the orientation of the axes. Graphics device interface (GDI) makes adjustments as necessary to ensure the x and y units remain the same size (When the window extent is set, the viewport will be adjusted to keep the units isotropic).

</td>
</tr>
<tr>
<td width="40%"><a id="MM_LOENGLISH"></a><a id="mm_loenglish"></a><dl>
<dt><b>MM_LOENGLISH</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.01 inch. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_LOMETRIC"></a><a id="mm_lometric"></a><dl>
<dt><b>MM_LOMETRIC</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to 0.1 millimeter. Positive x is to the right; positive y is up.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_TEXT"></a><a id="mm_text"></a><dl>
<dt><b>MM_TEXT</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to one device pixel. Positive x is to the right; positive y is down.

</td>
</tr>
<tr>
<td width="40%"><a id="MM_TWIPS"></a><a id="mm_twips"></a><dl>
<dt><b>MM_TWIPS</b></dt>
</dl>
</td>
<td width="60%">
Each logical unit is mapped to one twentieth of a printer's point (1/1440 inch, also called a twip). Positive x is to the right; positive y is up.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value identifies the previous mapping mode.

If the function fails, the return value is zero.

## -remarks

The MM_TEXT mode allows applications to work in device pixels, whose size varies from device to device.

The MM_HIENGLISH, MM_HIMETRIC, MM_LOENGLISH, MM_LOMETRIC, and MM_TWIPS modes are useful for applications drawing in physically meaningful units (such as inches or millimeters).

The MM_ISOTROPIC mode ensures a 1:1 aspect ratio.

The MM_ANISOTROPIC mode allows the x-coordinates and y-coordinates to be adjusted independently.


#### Examples

For an example, see <a href="/windows/desktop/gdi/using-coordinate-spaces-and-transformations">Using Coordinate Spaces and Transformations</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getmapmode">GetMapMode</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportextex">SetViewportExtEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindowextex">SetWindowExtEx</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setwindoworgex">SetWindowOrgEx</a>