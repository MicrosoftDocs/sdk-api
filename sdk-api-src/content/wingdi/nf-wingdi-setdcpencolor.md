---
UID: NF:wingdi.SetDCPenColor
title: SetDCPenColor function (wingdi.h)
description: SetDCPenColor function sets the current device context (DC) pen color to the specified color value. If the device cannot represent the specified color value, the color is set to the nearest physical color.
helpviewer_keywords: ["SetDCPenColor","SetDCPenColor function [Windows GDI]","_win32_SetDCPenColor","gdi.setdcpencolor","wingdi/SetDCPenColor"]
old-location: gdi\setdcpencolor.htm
tech.root: gdi
ms.assetid: 057608eb-7209-4714-bf02-660a13d59016
ms.date: 12/05/2018
ms.keywords: SetDCPenColor, SetDCPenColor function [Windows GDI], _win32_SetDCPenColor, gdi.setdcpencolor, wingdi/SetDCPenColor
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
 - SetDCPenColor
 - wingdi/SetDCPenColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - SetDCPenColor
---

# SetDCPenColor function


## -description

<b>SetDCPenColor</b> function sets the current device context (DC) pen color to the specified color value. If the device cannot represent the specified color value, the color is set to the nearest physical color.

## -parameters

### -param hdc [in]

A handle to the DC.

### -param color [in]

The new pen color.

## -returns

If the function succeeds, the return value specifies the previous DC pen color as a <a href="/windows/desktop/gdi/colorref">COLORREF</a> value. If the function fails, the return value is CLR_INVALID.

## -remarks

The function returns the previous DC_PEN color, even if the stock pen DC_PEN is not selected in the DC; however, this will not be used in drawing operations until the stock DC_PEN is selected in the DC.

The <a href="/windows/desktop/api/wingdi/nf-wingdi-getstockobject">GetStockObject</a> function with an argument of DC_BRUSH or DC_PEN can be used interchangeably with the <b>SetDCPenColor</b> and <a href="/windows/desktop/api/wingdi/nf-wingdi-setdcbrushcolor">SetDCBrushColor</a> functions.

<b>ICM:</b> Color management is performed if ICM is enabled.


#### Examples

For an example of setting colors, see <a href="/windows/desktop/gdi/setting-the-pen-or-brush-color">Setting the Pen or Brush Color</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/gdi/colorref">COLORREF</a>



<a href="/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdcpencolor">GetDCPenColor
      </a>