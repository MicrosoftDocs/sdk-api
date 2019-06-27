---
UID: NF:wingdi.GetNearestPaletteIndex
title: GetNearestPaletteIndex function (wingdi.h)
author: windows-sdk-content
description: The GetNearestPaletteIndex function retrieves the index for the entry in the specified logical palette most closely matching a specified color value.
old-location: gdi\getnearestpaletteindex.htm
tech.root: gdi
ms.assetid: df54532d-dcdb-4927-8f48-c9c92a7e0121
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNearestPaletteIndex, GetNearestPaletteIndex function [Windows GDI], _win32_GetNearestPaletteIndex, gdi.getnearestpaletteindex, wingdi/GetNearestPaletteIndex
ms.topic: function
f1_keywords: 
 - "wingdi/GetNearestPaletteIndex"
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
 - Ext-MS-Win-GDI-DC-L1-2-1.dll
 - GDI32Full.dll
api_name:
 - GetNearestPaletteIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetNearestPaletteIndex function


## -description


The <b>GetNearestPaletteIndex</b> function retrieves the index for the entry in the specified logical palette most closely matching a specified color value.


## -parameters




### -param h [in]

A handle to a logical palette.


### -param color [in]

A color to be matched. To create a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> color value, use the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a> macro.


## -returns



If the function succeeds, the return value is the index of an entry in a logical palette.

If the function fails, the return value is CLR_INVALID.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

If the given logical palette contains entries with the PC_EXPLICIT flag set, the return value is undefined.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/color-functions">Color Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/colors">Colors Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps">GetDeviceCaps</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getnearestcolor">GetNearestColor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getpaletteentries">GetPaletteEntries</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getsystempaletteentries">GetSystemPaletteEntries</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-rgb">RGB</a>
 

 

