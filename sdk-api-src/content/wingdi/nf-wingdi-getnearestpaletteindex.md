---
UID: NF:wingdi.GetNearestPaletteIndex
title: GetNearestPaletteIndex function
author: windows-sdk-content
description: The GetNearestPaletteIndex function retrieves the index for the entry in the specified logical palette most closely matching a specified color value.
old-location: gdi\getnearestpaletteindex.htm
tech.root: gdi
ms.assetid: df54532d-dcdb-4927-8f48-c9c92a7e0121
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNearestPaletteIndex, GetNearestPaletteIndex function [Windows GDI], _win32_GetNearestPaletteIndex, gdi.getnearestpaletteindex, wingdi/GetNearestPaletteIndex
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
 - Ext-MS-Win-GDI-DC-L1-2-1.dll
 - GDI32Full.dll
api_name:
 - GetNearestPaletteIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetNearestPaletteIndex function


## -description


The <b>GetNearestPaletteIndex</b> function retrieves the index for the entry in the specified logical palette most closely matching a specified color value.


## -parameters




### -param h [in]

A handle to a logical palette.


### -param color [in]

A color to be matched. To create a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> color value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value is the index of an entry in a logical palette.

If the function fails, the return value is CLR_INVALID.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

If the given logical palette contains entries with the PC_EXPLICIT flag set, the return value is undefined.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/89e4e19b-47be-442e-8eb4-c867bb78f36a">GetNearestColor</a>



<a href="https://msdn.microsoft.com/5e72e881-32e1-458e-a09e-91fa13abe178">GetPaletteEntries</a>



<a href="https://msdn.microsoft.com/67bb0adf-ae7f-48d5-bc62-82ece45aeee6">GetSystemPaletteEntries</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>
 

 

