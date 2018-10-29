---
UID: NF:winuser.GrayStringW
title: GrayStringW function
author: windows-sdk-content
description: The GrayString function draws gray text at the specified location.
old-location: gdi\graystring.htm
tech.root: gdi
ms.assetid: b14b8c40-f97f-4e41-8d8d-687692acfda9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GrayString, GrayString function [Windows GDI], GrayStringA, GrayStringW, _win32_GrayString, gdi.graystring, winuser/GrayString, winuser/GrayStringA, winuser/GrayStringW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GrayStringW (Unicode) and GrayStringA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - GrayString
 - GrayStringA
 - GrayStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GrayStringW function


## -description


The <b>GrayString</b> function draws gray text at the specified location. The function draws the text by copying it into a memory bitmap, graying the bitmap, and then copying the bitmap to the screen. The function grays the text regardless of the selected brush and background. <b>GrayString</b> uses the font currently selected for the specified device context.

If thelpOutputFuncparameter is <b>NULL</b>, GDI uses the <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> function, and thelpDataparameter is assumed to be a pointer to the character string to be output. If the characters to be output cannot be handled by <b>TextOut</b> (for example, the string is stored as a bitmap), the application must supply its own output function.


## -parameters




### -param hDC [in]

A handle to the device context.


### -param hBrush [in]

A handle to the brush to be used for graying. If this parameter is <b>NULL</b>, the text is grayed with the same brush that was used to draw window text.


### -param lpOutputFunc [in]

A pointer to the application-defined function that will draw the string, or, if <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> is to be used to draw the string, it is a <b>NULL</b> pointer. For details, see the <a href="https://msdn.microsoft.com/4d9145d2-5be4-4da3-9d03-01ebd74e0d06">OutputProc</a> callback function.


### -param lpData [in]

A pointer to data to be passed to the output function. If the <i>lpOutputFunc</i> parameter is <b>NULL</b>, <i>lpData</i> must be a pointer to the string to be output.


### -param nCount [in]

The number of characters to be output. If the <i>nCount</i> parameter is zero, <b>GrayString</b> calculates the length of the string (assuming <i>lpData</i> is a pointer to the string). If <i>nCount</i> is 1 and the function pointed to by <i>lpOutputFunc</i> returns <b>FALSE</b>, the image is shown but not grayed.


### -param X [in]

The device x-coordinate of the starting position of the rectangle that encloses the string.


### -param Y [in]

The device y-coordinate of the starting position of the rectangle that encloses the string.


### -param nWidth [in]

The width, in device units, of the rectangle that encloses the string. If this parameter is zero, <b>GrayString</b> calculates the width of the area, assuming <i>lpData</i> is a pointer to the string.


### -param nHeight [in]

The height, in device units, of the rectangle that encloses the string. If this parameter is zero, <b>GrayString</b> calculates the height of the area, assuming <i>lpData</i> is a pointer to the string.


## -returns



If the string is drawn, the return value is nonzero.

If either the <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> function or the application-defined output function returned zero, or there was insufficient memory to create a memory bitmap for graying, the return value is zero.




## -remarks



Without calling <b>GrayString</b>, an application can draw grayed strings on devices that support a solid gray color. The system color COLOR_GRAYTEXT is the solid-gray system color used to draw disabled text. The application can call the <a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a> function to retrieve the color value of COLOR_GRAYTEXT. If the color is other than zero (black), the application can call the <a href="https://msdn.microsoft.com/3875a247-7c32-4917-bf6d-50b2a49848a6">SetTextColor</a> function to set the text color to the color value and then draw the string directly. If the retrieved color is black, the application must call <b>GrayString</b> to gray the text.




## -see-also




<a href="https://msdn.microsoft.com/fe412280-d797-4abd-8a29-107a9cd96145">DrawText</a>



<a href="https://msdn.microsoft.com/165c1781-161e-4ab2-98c9-eec4e9098d09">GetSysColor</a>



<a href="https://msdn.microsoft.com/4d9145d2-5be4-4da3-9d03-01ebd74e0d06">OutputProc</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/3875a247-7c32-4917-bf6d-50b2a49848a6">SetTextColor</a>



<a href="https://msdn.microsoft.com/1cb78a75-752d-4e06-afdf-cd797f209114">TabbedTextOut</a>



<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
 

 

