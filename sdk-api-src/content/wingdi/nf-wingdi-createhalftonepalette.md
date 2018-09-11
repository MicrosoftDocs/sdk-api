---
UID: NF:wingdi.CreateHalftonePalette
title: CreateHalftonePalette function
author: windows-sdk-content
description: The CreateHalftonePalette function creates a halftone palette for the specified device context (DC).
old-location: gdi\createhalftonepalette.htm
tech.root: gdi
ms.assetid: ba9dfa0c-98df-4922-acba-d00e9b4b0fb0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreateHalftonePalette, CreateHalftonePalette function [Windows GDI], _win32_CreateHalftonePalette, gdi.createhalftonepalette, wingdi/CreateHalftonePalette
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
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - CreateHalftonePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateHalftonePalette function


## -description


The <b>CreateHalftonePalette</b> function creates a halftone palette for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is a handle to a logical halftone palette.

If the function fails, the return value is zero.




## -remarks



An application should create a halftone palette when the stretching mode of a device context is set to HALFTONE. The logical halftone palette returned by <b>CreateHalftonePalette</b> should then be selected and realized into the device context before the <a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a> or <a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a> function is called.

When you no longer need the palette, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>



<a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a>



<a href="https://msdn.microsoft.com/3e5a48dc-ccd5-41ea-a24b-5c40213abf38">SetStretchBltMode</a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a>



<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a>
 

 

