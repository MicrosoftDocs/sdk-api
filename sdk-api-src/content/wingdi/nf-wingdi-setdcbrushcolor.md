---
UID: NF:wingdi.SetDCBrushColor
title: SetDCBrushColor function (wingdi.h)
description: SetDCBrushColor function sets the current device context (DC) brush color to the specified color value. If the device cannot represent the specified color value, the color is set to the nearest physical color.
helpviewer_keywords: ["SetDCBrushColor","SetDCBrushColor function [Windows GDI]","_win32_SetDCBrushColor","gdi.setdcbrushcolor","wingdi/SetDCBrushColor"]
old-location: gdi\setdcbrushcolor.htm
tech.root: gdi
ms.assetid: 4feed536-2f1d-4a25-8311-7cae303167ca
ms.date: 12/05/2018
ms.keywords: SetDCBrushColor, SetDCBrushColor function [Windows GDI], _win32_SetDCBrushColor, gdi.setdcbrushcolor, wingdi/SetDCBrushColor
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
 - SetDCBrushColor
 - wingdi/SetDCBrushColor
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
 - SetDCBrushColor
---

# SetDCBrushColor function


## -description

<b>SetDCBrushColor</b> function sets the current device context (DC) brush color to the specified color value. If the device cannot represent the specified color value, the color is set to the nearest physical color.

## -parameters

### -param hdc [in]

A handle to the DC.

### -param color [in]

The new brush color.

## -returns

If the function succeeds, the return value specifies the previous DC brush color as a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID.

## -remarks

When the stock DC_BRUSH is selected in a DC, all the subsequent drawings will be done using the DC brush color until the stock brush is deselected. The default DC_BRUSH color is WHITE.

The function returns the previous DC_BRUSH color, even if the stock brush DC_BRUSH is not selected in the DC: however, this will not be used in drawing operations until the stock DC_BRUSH is selected in the DC.

The <a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject</a> function with an argument of DC_BRUSH or DC_PEN can be used interchangeably with the <a href="/windows/desktop/api/wingdi/nf-wingdi-setdcpencolor">SetDCPenColor</a> and <b>SetDCBrushColor</b> functions.

<b>ICM:</b> Color management is performed if ICM is enabled.


#### Examples

For an example of setting colors, see <a href="/windows/desktop/gdi/setting-the-pen-or-brush-color">Setting the Pen or Brush Color</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdcbrushcolor">GetDCBrushColor
      </a>