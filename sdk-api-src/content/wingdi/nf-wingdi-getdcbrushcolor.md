---
UID: NF:wingdi.GetDCBrushColor
title: GetDCBrushColor function (wingdi.h)
description: The GetDCBrushColor function retrieves the current brush color for the specified device context (DC).
old-location: gdi\getdcbrushcolor.htm
tech.root: gdi
ms.assetid: 98844fb1-7ad8-4fbd-be59-9a19065253da
ms.date: 12/05/2018
ms.keywords: GetDCBrushColor, GetDCBrushColor function [Windows GDI], _win32_GetDCBrushColor, gdi.getdcbrushcolor, wingdi/GetDCBrushColor
f1_keywords:
- wingdi/GetDCBrushColor
dev_langs:
- c++
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
- Gdi32.dll
- ext-ms-win-gdi-dc-l1-2-1.dll
- GDI32Full.dll
api_name:
- GetDCBrushColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDCBrushColor function


## -description


The <b>GetDCBrushColor</b> function retrieves the current brush color for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the DC whose brush color is to be returned.


## -returns



If the function succeeds, the return value is the <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> value for the current DC brush color.

If the function fails, the return value is CLR_INVALID.




## -remarks



For information on setting the brush color, see <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setdcbrushcolor">SetDCBrushColor</a>.

<b>ICM:</b> Color management is performed if ICM is enabled.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setdcbrushcolor">SetDCBrushColor</a>
 

 

