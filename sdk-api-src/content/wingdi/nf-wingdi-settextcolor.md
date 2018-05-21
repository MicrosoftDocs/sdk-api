---
UID: NF:wingdi.SetTextColor
title: SetTextColor function
author: windows-driver-content
description: The SetTextColor function sets the text color for the specified device context to the specified color.
old-location: gdi\settextcolor.htm
old-project: gdi
ms.assetid: 3875a247-7c32-4917-bf6d-50b2a49848a6
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: SetTextColor, SetTextColor function [Windows GDI], _win32_SetTextColor, gdi.settextcolor, wingdi/SetTextColor
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Font-l1-1-1.dll
-	ext-ms-win-gdi-font-l1-1-2.dll
-	Ext-MS-Win-GDI-Font-L1-1-0.dll
-	Ext-MS-Win-GDI-Font-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	SetTextColor
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetTextColor function


## -description


The <b>SetTextColor</b> function sets the text color for the specified device context to the specified color.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param color

TBD




#### - crColor [in]

The color of the text.


## -returns



If the function succeeds, the return value is a color reference for the previous text color as a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID.




## -remarks



The text color is used to draw the face of each character written by the <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> and <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> functions. The text color is also used in converting bitmaps from color to monochrome and vice versa.


#### Examples

For an example, see "Setting Fonts for Menu-Item Text Strings" in <a href="_win32_Using_Menus_cpp">Using Menus</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d6a181e4-b6cf-44b7-bf47-4900272d6d72">BitBlt</a>



<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/d3d91b86-5143-431a-ba18-b951b832d7b6">GetTextColor</a>



<a href="https://msdn.microsoft.com/e1dcb5f8-c026-4a4e-8541-928a057bf0ae">RGB</a>



<a href="https://msdn.microsoft.com/9163370b-19c5-4c23-9197-793e4b8d50c4">SetBkColor</a>



<a href="https://msdn.microsoft.com/5130c88e-08e8-4faa-a1cb-a8106c86cea0">StretchBlt</a>



<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
 

 

