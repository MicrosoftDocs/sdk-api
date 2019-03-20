---
UID: NF:wingdi.RealizePalette
title: RealizePalette function (wingdi.h)
author: windows-sdk-content
description: The RealizePalette function maps palette entries from the current logical palette to the system palette.
old-location: gdi\realizepalette.htm
tech.root: gdi
ms.assetid: 1c744ad2-09bc-455f-bc3c-9a2583b57a30
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RealizePalette, RealizePalette function [Windows GDI], _win32_RealizePalette, gdi.realizepalette, wingdi/RealizePalette
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
 - ext-ms-win-gdi-dc-l1-2-1.dll
 - GDI32Full.dll
api_name:
 - RealizePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RealizePalette function


## -description


The <b>RealizePalette</b> function maps palette entries from the current logical palette to the system palette.


## -parameters




### -param hdc [in]

A handle to the device context into which a logical palette has been selected.


## -returns



If the function succeeds, the return value is the number of entries in the logical palette mapped to the system palette.

If the function fails, the return value is GDI_ERROR.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

The <b>RealizePalette</b> function modifies the palette for the device associated with the specified device context. If the device context is a memory DC, the color table for the bitmap selected into the DC is modified. If the device context is a display DC, the physical palette for that device is modified.

A logical palette is a buffer between color-intensive applications and the system, allowing these applications to use as many colors as needed without interfering with colors displayed by other windows.

When an application's window has the focus and it calls the <b>RealizePalette</b> function, the system attempts to realize as many of the requested colors as possible. The same is also true for applications with inactive windows.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/f3462198-9360-4b77-ac62-9fe21ec666be">CreatePalette</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a>
 

 

