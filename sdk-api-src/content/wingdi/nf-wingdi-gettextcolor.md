---
UID: NF:wingdi.GetTextColor
title: GetTextColor function
author: windows-sdk-content
description: The GetTextColor function retrieves the current text color for the specified device context.
old-location: gdi\gettextcolor.htm
tech.root: gdi
ms.assetid: d3d91b86-5143-431a-ba18-b951b832d7b6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTextColor, GetTextColor function [Windows GDI], _win32_GetTextColor, gdi.gettextcolor, wingdi/GetTextColor
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
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetTextColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetTextColor
: 
---

# GetTextColor function


## -description


The <b>GetTextColor</b> function retrieves the current text color for the specified device context.


## -parameters




### -param hdc [in]

Handle to the device context.


## -returns



If the function succeeds, the return value is the current text color as a <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> value.

If the function fails, the return value is CLR_INVALID. No extended error information is available.




## -remarks



The text color defines the foreground color of characters drawn by using the <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> or <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>



<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/3875a247-7c32-4917-bf6d-50b2a49848a6">SetTextColor</a>



<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
 

 

