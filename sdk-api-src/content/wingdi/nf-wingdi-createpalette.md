---
UID: NF:wingdi.CreatePalette
title: CreatePalette function
author: windows-sdk-content
description: The CreatePalette function creates a logical palette.
old-location: gdi\createpalette.htm
old-project: gdi
ms.assetid: f3462198-9360-4b77-ac62-9fe21ec666be
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreatePalette, CreatePalette function [Windows GDI], _win32_CreatePalette, gdi.createpalette, wingdi/CreatePalette
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
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
 - CreatePalette
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreatePalette function


## -description


The <b>CreatePalette</b> function creates a logical palette.


## -parameters




### -param plpal [in]

A pointer to a <a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a> structure that contains information about the colors in the logical palette.


## -returns



If the function succeeds, the return value is a handle to a logical palette.

If the function fails, the return value is <b>NULL</b>.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

Once an application creates a logical palette, it can select that palette into a device context by calling the <a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a> function. A palette selected into a device context can be realized by calling the <a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a> function.

When you no longer need the palette, call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/99d70a0e-ac61-4a88-a500-66443e7882ad">LOGPALETTE</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>



<a href="https://msdn.microsoft.com/1fc3356f-6fa3-444f-b224-b953acd2394b">SelectPalette</a>
 

 

