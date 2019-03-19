---
UID: NF:wingdi.SetBkColor
title: SetBkColor function (wingdi.h)
author: windows-sdk-content
description: The SetBkColor function sets the current background color to the specified color value, or to the nearest physical color if the device cannot represent the specified color value.
old-location: gdi\setbkcolor.htm
tech.root: gdi
ms.assetid: 9163370b-19c5-4c23-9197-793e4b8d50c4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetBkColor, SetBkColor function [Windows GDI], _win32_SetBkColor, gdi.setbkcolor, wingdi/SetBkColor
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
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-0.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetBkColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetBkColor function


## -description


The <b>SetBkColor</b> function sets the current background color to the specified color value, or to the nearest physical color if the device cannot represent the specified color value.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param color [in]

The new background color. To make a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value, use the <a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a> macro.


## -returns



If the function succeeds, the return value specifies the previous background color as a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID.




## -remarks



This function fills the gaps between styled lines drawn using a pen created by the <a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a> function; it does not fill the gaps between styled lines drawn using a pen created by the <a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a> function. The <b>SetBkColor</b> function also sets the background colors for <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> and <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>.

If the background mode is OPAQUE, the background color is used to fill gaps between styled lines, gaps between hatched lines in brushes, and character cells. The background color is also used when converting bitmaps from color to monochrome and vice versa.


#### Examples

For an example, see "Example of Owner-Drawn Menu Items" in <a href="https://msdn.microsoft.com/en-us/library/ms647558(v=VS.85).aspx">Using Menus</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/882facd2-7e06-48f6-82e4-f20e4d5adc92">CreatePen</a>



<a href="https://msdn.microsoft.com/a1e81314-4fe6-481f-af96-24ebf56332cf">ExtCreatePen</a>



<a href="https://msdn.microsoft.com/1c6e8d05-4b8d-476d-852c-f06f316cb8b7">GetBKColor</a>



<a href="https://msdn.microsoft.com/3faedb48-3163-48fd-b26e-712de9c4bfaf">GetBkMode</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/60e4467a-14ab-421e-b174-4b9c0134ce72">SetBkMode</a>
 

 

