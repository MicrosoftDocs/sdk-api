---
UID: NF:wingdi.GetCharWidthFloatA
title: GetCharWidthFloatA function
author: windows-driver-content
description: The GetCharWidthFloat function retrieves the fractional widths of consecutive characters in a specified range from the current font.
old-location: gdi\getcharwidthfloat.htm
old-project: gdi
ms.assetid: 7a90b701-63f9-41e5-9069-10d344edfe02
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetCharWidthFloat, GetCharWidthFloat function [Windows GDI], GetCharWidthFloatA, GetCharWidthFloatW, _win32_GetCharWidthFloat, gdi.getcharwidthfloat, wingdi/GetCharWidthFloat, wingdi/GetCharWidthFloatA, wingdi/GetCharWidthFloatW
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
req.unicode-ansi: GetCharWidthFloatW (Unicode) and GetCharWidthFloatA (ANSI)
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
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetCharWidthFloat
-	GetCharWidthFloatA
-	GetCharWidthFloatW
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCharWidthFloatA function


## -description


The <b>GetCharWidthFloat</b> function retrieves the fractional widths of consecutive characters in a specified range from the current font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param iFirst

TBD


### -param iLast

TBD


### -param lpBuffer

TBD




#### - iFirstChar [in]

The code point of the first character in the group of consecutive characters.


#### - iLastChar [in]

The code point of the last character in the group of consecutive characters.


#### - pxBuffer [out]

A pointer to a buffer that receives the character widths, in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The returned widths are in the 32-bit IEEE floating-point format. (The widths are measured along the base line of the characters.)

If the <i>iFirstChar</i> parameter specifies the letter a and the <i>iLastChar</i> parameter specifies the letter z, <b>GetCharWidthFloat</b> retrieves the widths of all lowercase characters.

If a character does not exist in the current font, it is assigned the width of the default character.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>



<a href="https://msdn.microsoft.com/552942c9-e2a6-43f9-901f-3aba1e2523e5">GetCharABCWidthsFloat</a>



<a href="https://msdn.microsoft.com/f7d6e9b3-72aa-42d8-8346-b230b9e98237">GetCharWidth32</a>
 

 

