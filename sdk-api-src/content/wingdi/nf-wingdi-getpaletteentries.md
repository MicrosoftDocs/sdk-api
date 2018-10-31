---
UID: NF:wingdi.GetPaletteEntries
title: GetPaletteEntries function
author: windows-sdk-content
description: The GetPaletteEntries function retrieves a specified range of palette entries from the given logical palette.
old-location: gdi\getpaletteentries.htm
tech.root: gdi
ms.assetid: 5e72e881-32e1-458e-a09e-91fa13abe178
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetPaletteEntries, GetPaletteEntries function [Windows GDI], _win32_GetPaletteEntries, gdi.getpaletteentries, wingdi/GetPaletteEntries
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
 - GetPaletteEntries
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPaletteEntries function


## -description


The <b>GetPaletteEntries</b> function retrieves a specified range of palette entries from the given logical palette.


## -parameters




### -param hpal [in]

A handle to the logical palette.


### -param iStart [in]

The first entry in the logical palette to be retrieved.


### -param cEntries [in]

The number of entries in the logical palette to be retrieved.


### -param pPalEntries [out]

A pointer to an array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures to receive the palette entries. The array must contain at least as many structures as specified by the <i>nEntries</i> parameter.


## -returns



If the function succeeds and the handle to the logical palette is a valid pointer (not <b>NULL</b>), the return value is the number of entries retrieved from the logical palette. If the function succeeds and handle to the logical palette is <b>NULL</b>, the return value is the number of entries in the given palette.

If the function fails, the return value is zero.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

If the <i>nEntries</i> parameter specifies more entries than exist in the palette, the remaining members of the <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structure are not altered.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/67bb0adf-ae7f-48d5-bc62-82ece45aeee6">GetSystemPaletteEntries</a>



<a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a>



<a href="https://msdn.microsoft.com/df38f482-75ba-4800-8b26-92204c63255e">SetPaletteEntries</a>
 

 

