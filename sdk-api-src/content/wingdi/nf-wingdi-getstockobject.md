---
UID: NF:wingdi.GetStockObject
title: GetStockObject function
author: windows-sdk-content
description: The GetStockObject function retrieves a handle to one of the stock pens, brushes, fonts, or palettes.
old-location: gdi\getstockobject.htm
tech.root: gdi
ms.assetid: b14ddc05-7e7b-4fc6-b7e3-efe892df7e21
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ANSI_FIXED_FONT, ANSI_VAR_FONT, BLACK_BRUSH, BLACK_PEN, DC_BRUSH, DC_PEN, DEFAULT_GUI_FONT, DEFAULT_PALETTE, DEVICE_DEFAULT_FONT, DKGRAY_BRUSH, GRAY_BRUSH, GetStockObject, GetStockObject function [Windows GDI], HOLLOW_BRUSH, LTGRAY_BRUSH, NULL_BRUSH, NULL_PEN, OEM_FIXED_FONT, SYSTEM_FIXED_FONT, SYSTEM_FONT, WHITE_BRUSH, WHITE_PEN, _win32_GetStockObject, gdi.getstockobject, wingdi/GetStockObject
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
 - Ext-MS-Win-GDI-DC-l1-2-0.dll
 - ext-ms-win-gdi-dc-l1-1-0.dll
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - GetStockObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetStockObject function


## -description


The <b>GetStockObject</b> function retrieves a handle to one of the stock pens, brushes, fonts, or palettes.


## -parameters




### -param i [in]

The type of stock object. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BLACK_BRUSH"></a><a id="black_brush"></a><dl>
<dt><b>BLACK_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Black brush.

</td>
</tr>
<tr>
<td width="40%"><a id="DKGRAY_BRUSH"></a><a id="dkgray_brush"></a><dl>
<dt><b>DKGRAY_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Dark gray brush.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_BRUSH"></a><a id="dc_brush"></a><dl>
<dt><b>DC_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Solid color brush. The default color is white. The color can be changed by using the <a href="https://msdn.microsoft.com/4feed536-2f1d-4a25-8311-7cae303167ca">SetDCBrushColor</a> function. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="GRAY_BRUSH"></a><a id="gray_brush"></a><dl>
<dt><b>GRAY_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Gray brush.

</td>
</tr>
<tr>
<td width="40%"><a id="HOLLOW_BRUSH"></a><a id="hollow_brush"></a><dl>
<dt><b>HOLLOW_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Hollow brush (equivalent to NULL_BRUSH).

</td>
</tr>
<tr>
<td width="40%"><a id="LTGRAY_BRUSH"></a><a id="ltgray_brush"></a><dl>
<dt><b>LTGRAY_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Light gray brush.

</td>
</tr>
<tr>
<td width="40%"><a id="NULL_BRUSH"></a><a id="null_brush"></a><dl>
<dt><b>NULL_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
Null brush (equivalent to HOLLOW_BRUSH).

</td>
</tr>
<tr>
<td width="40%"><a id="WHITE_BRUSH"></a><a id="white_brush"></a><dl>
<dt><b>WHITE_BRUSH</b></dt>
</dl>
</td>
<td width="60%">
White brush.

</td>
</tr>
<tr>
<td width="40%"><a id="BLACK_PEN"></a><a id="black_pen"></a><dl>
<dt><b>BLACK_PEN</b></dt>
</dl>
</td>
<td width="60%">
Black pen.

</td>
</tr>
<tr>
<td width="40%"><a id="DC_PEN"></a><a id="dc_pen"></a><dl>
<dt><b>DC_PEN</b></dt>
</dl>
</td>
<td width="60%">
Solid pen color. The default color is white. The color can be changed by using the <a href="https://msdn.microsoft.com/057608eb-7209-4714-bf02-660a13d59016">SetDCPenColor</a> function. For more information, see the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="NULL_PEN"></a><a id="null_pen"></a><dl>
<dt><b>NULL_PEN</b></dt>
</dl>
</td>
<td width="60%">
Null pen. The null pen draws nothing.

</td>
</tr>
<tr>
<td width="40%"><a id="WHITE_PEN"></a><a id="white_pen"></a><dl>
<dt><b>WHITE_PEN</b></dt>
</dl>
</td>
<td width="60%">
White pen.

</td>
</tr>
<tr>
<td width="40%"><a id="ANSI_FIXED_FONT"></a><a id="ansi_fixed_font"></a><dl>
<dt><b>ANSI_FIXED_FONT</b></dt>
</dl>
</td>
<td width="60%">
Windows fixed-pitch (monospace) system font.

</td>
</tr>
<tr>
<td width="40%"><a id="ANSI_VAR_FONT"></a><a id="ansi_var_font"></a><dl>
<dt><b>ANSI_VAR_FONT</b></dt>
</dl>
</td>
<td width="60%">
Windows variable-pitch (proportional space) system font.

</td>
</tr>
<tr>
<td width="40%"><a id="DEVICE_DEFAULT_FONT"></a><a id="device_default_font"></a><dl>
<dt><b>DEVICE_DEFAULT_FONT</b></dt>
</dl>
</td>
<td width="60%">
Device-dependent font.

</td>
</tr>
<tr>
<td width="40%"><a id="DEFAULT_GUI_FONT"></a><a id="default_gui_font"></a><dl>
<dt><b>DEFAULT_GUI_FONT</b></dt>
</dl>
</td>
<td width="60%">
Default font for user interface objects such as menus and dialog boxes. It is not recommended that you use DEFAULT_GUI_FONT or SYSTEM_FONT to obtain the font used by dialogs and windows; for more information, see the remarks section.

The default font is Tahoma.

</td>
</tr>
<tr>
<td width="40%"><a id="OEM_FIXED_FONT"></a><a id="oem_fixed_font"></a><dl>
<dt><b>OEM_FIXED_FONT</b></dt>
</dl>
</td>
<td width="60%">
Original equipment manufacturer (OEM) dependent fixed-pitch (monospace) font.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_FONT"></a><a id="system_font"></a><dl>
<dt><b>SYSTEM_FONT</b></dt>
</dl>
</td>
<td width="60%">
System font. By default, the system uses the system font to draw menus, dialog box controls, and text. It is not recommended that you use DEFAULT_GUI_FONT or SYSTEM_FONT to obtain the font used by dialogs and windows; for more information, see the remarks section. 

The default system font is Tahoma.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_FIXED_FONT"></a><a id="system_fixed_font"></a><dl>
<dt><b>SYSTEM_FIXED_FONT</b></dt>
</dl>
</td>
<td width="60%">
Fixed-pitch (monospace) system font. This stock object is provided only for compatibility with 16-bit Windows versions earlier than 3.0.

</td>
</tr>
<tr>
<td width="40%"><a id="DEFAULT_PALETTE"></a><a id="default_palette"></a><dl>
<dt><b>DEFAULT_PALETTE</b></dt>
</dl>
</td>
<td width="60%">
Default palette. This palette consists of the static colors in the system palette.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is a handle to the requested logical object.

If the function fails, the return value is <b>NULL</b>.




## -remarks



It is not recommended that you employ this method to obtain the current font used by dialogs and windows. Instead, use the <a href="http://msdn.microsoft.com/en-us/library/ms724947.aspx">SystemParametersInfo</a> function with the SPI_GETNONCLIENTMETRICS parameter to retrieve the current font. <a href="http://msdn.microsoft.com/en-us/library/ms724947.aspx">SystemParametersInfo</a> will take into account the current theme and provides font information for captions, menus, and message dialogs. 

Use the DKGRAY_BRUSH, GRAY_BRUSH, and LTGRAY_BRUSH stock objects only in windows with the CS_HREDRAW and CS_VREDRAW styles. Using a gray stock brush in any other style of window can lead to misalignment of brush patterns after a window is moved or sized. The origins of stock brushes cannot be adjusted.

The HOLLOW_BRUSH and NULL_BRUSH stock objects are equivalent.

It is not necessary (but it is not harmful) to delete stock objects by calling <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>.

Both DC_BRUSH and DC_PEN can be used interchangeably with other stock objects like BLACK_BRUSH and BLACK_PEN. For information on retrieving the current pen or brush color, see <a href="https://msdn.microsoft.com/98844fb1-7ad8-4fbd-be59-9a19065253da">GetDCBrushColor</a> and <a href="https://msdn.microsoft.com/3a1d579f-fbc6-4021-a37e-0184b2cc7d5d">GetDCPenColor</a>. See <a href="https://msdn.microsoft.com/d1be1db8-e6b6-4d60-8a4a-ce218f8d52fc">Setting the Pen or Brush Color</a> for an example of setting colors. The <b>GetStockObject</b> function with an argument of DC_BRUSH or DC_PEN can be used interchangeably with the <a href="https://msdn.microsoft.com/057608eb-7209-4714-bf02-660a13d59016">SetDCPenColor</a> and <a href="https://msdn.microsoft.com/4feed536-2f1d-4a25-8311-7cae303167ca">SetDCBrushColor</a> functions.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/d1be1db8-e6b6-4d60-8a4a-ce218f8d52fc">Setting the Pen or Brush Color</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

