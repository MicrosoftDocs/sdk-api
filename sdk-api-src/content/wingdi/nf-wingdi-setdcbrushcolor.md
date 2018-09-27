---
UID: NF:wingdi.SetDCBrushColor
title: SetDCBrushColor function
author: windows-sdk-content
description: SetDCBrushColor function sets the current device context (DC) brush color to the specified color value. If the device cannot represent the specified color value, the color is set to the nearest physical color.
old-location: gdi\setdcbrushcolor.htm
tech.root: gdi
ms.assetid: 4feed536-2f1d-4a25-8311-7cae303167ca
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SetDCBrushColor, SetDCBrushColor function [Windows GDI], _win32_SetDCBrushColor, gdi.setdcbrushcolor, wingdi/SetDCBrushColor
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
 - SetDCBrushColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



If the function succeeds, the return value specifies the previous DC brush color as a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID.




## -remarks



When the stock DC_BRUSH is selected in a DC, all the subsequent drawings will be done using the DC brush color until the stock brush is deselected. The default DC_BRUSH color is WHITE.

The function returns the previous DC_BRUSH color, even if the stock brush DC_BRUSH is not selected in the DC: however, this will not be used in drawing operations until the stock DC_BRUSH is selected in the DC.

The <a href="https://msdn.microsoft.com/b14ddc05-7e7b-4fc6-b7e3-efe892df7e21">GetStockObject</a> function with an argument of DC_BRUSH or DC_PEN can be used interchangeably with the <a href="https://msdn.microsoft.com/057608eb-7209-4714-bf02-660a13d59016">SetDCPenColor</a> and <b>SetDCBrushColor</b> functions.

<b>ICM:</b> Color management is performed if ICM is enabled.


#### Examples

For an example of setting colors, see <a href="https://msdn.microsoft.com/d1be1db8-e6b6-4d60-8a4a-ce218f8d52fc">Setting the Pen or Brush Color</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/98844fb1-7ad8-4fbd-be59-9a19065253da">GetDCBrushColor
      </a>
 

 

