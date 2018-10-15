---
UID: NF:wingdi.UpdateColors
title: UpdateColors function
author: windows-sdk-content
description: The UpdateColors function updates the client area of the specified device context by remapping the current colors in the client area to the currently realized logical palette.
old-location: gdi\updatecolors.htm
tech.root: gdi
ms.assetid: 61dfd579-3fc9-4e0a-bfd9-d04c6f918fd8
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: UpdateColors, UpdateColors function [Windows GDI], _win32_UpdateColors, gdi.updatecolors, wingdi/UpdateColors
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - UpdateColors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UpdateColors function


## -description


The <b>UpdateColors</b> function updates the client area of the specified device context by remapping the current colors in the client area to the currently realized logical palette.


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

An inactive window with a realized logical palette may call <b>UpdateColors</b> as an alternative to redrawing its client area when the system palette changes.

The <b>UpdateColors</b> function typically updates a client area faster than redrawing the area. However, because <b>UpdateColors</b> performs the color translation based on the color of each pixel before the system palette changed, each call to this function results in the loss of some color accuracy.

This function must be called soon after a <a href="https://msdn.microsoft.com/2eed568b-1a16-47d2-ae26-3f1dec35e893">WM_PALETTECHANGED</a> message is received.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>



<a href="https://msdn.microsoft.com/1c744ad2-09bc-455f-bc3c-9a2583b57a30">RealizePalette</a>
 

 

