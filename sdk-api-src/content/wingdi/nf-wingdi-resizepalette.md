---
UID: NF:wingdi.ResizePalette
title: ResizePalette function
author: windows-sdk-content
description: The ResizePalette function increases or decreases the size of a logical palette based on the specified value.
old-location: gdi\resizepalette.htm
tech.root: gdi
ms.assetid: 77178869-cbfb-4b91-a5b0-7d0404e7534f
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ResizePalette, ResizePalette function [Windows GDI], _win32_ResizePalette, gdi.resizepalette, wingdi/ResizePalette
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
 - ResizePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ResizePalette
: 
---

# ResizePalette function


## -description


The <b>ResizePalette</b> function increases or decreases the size of a logical palette based on the specified value.


## -parameters




### -param hpal [in]

A handle to the palette to be changed.


### -param n [in]

The number of entries in the palette after it has been resized.

The number of entries is limited to 1024.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



An application can determine whether a device supports palette operations by calling the <a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a> function and specifying the RASTERCAPS constant.

If an application calls <b>ResizePalette</b> to reduce the size of the palette, the entries remaining in the resized palette are unchanged. If the application calls <b>ResizePalette</b> to enlarge the palette, the additional palette entries are set to black (the red, green, and blue values are all 0) and their flags are set to zero.




## -see-also




<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/d524c4c7-22af-495d-aecc-b9921e53ca7b">GetDeviceCaps</a>
 

 

