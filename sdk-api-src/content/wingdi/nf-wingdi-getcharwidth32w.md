---
UID: NF:wingdi.GetCharWidth32W
title: GetCharWidth32W function
author: windows-driver-content
description: The GetCharWidth32 function retrieves the widths, in logical coordinates, of consecutive characters in a specified range from the current font.
old-location: gdi\getcharwidth32.htm
old-project: gdi
ms.assetid: f7d6e9b3-72aa-42d8-8346-b230b9e98237
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetCharWidth32, GetCharWidth32 function [Windows GDI], GetCharWidth32A, GetCharWidth32W, _win32_GetCharWidth32, gdi.getcharwidth32, wingdi/GetCharWidth32, wingdi/GetCharWidth32A, wingdi/GetCharWidth32W
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
req.unicode-ansi: GetCharWidth32W (Unicode) and GetCharWidth32A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FAX_TIME, *PFAX_TIME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Font-l1-1-1.dll
-	ext-ms-win-gdi-font-l1-1-2.dll
-	Ext-MS-Win-GDI-Font-L1-1-3.dll
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32Full.dll
api_name:
-	GetCharWidth32
-	GetCharWidth32A
-	GetCharWidth32W
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCharWidth32W function


## -description


The <b>GetCharWidth32</b> function retrieves the widths, in logical coordinates, of consecutive characters in a specified range from the current font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param iFirst

TBD


### -param iLast

TBD


### -param lpBuffer [out]

A pointer to a buffer that receives the character widths, in logical coordinates.


#### - iFirstChar [in]

The first character in the group of consecutive characters.


#### - iLastChar [in]

The last character in the group of consecutive characters, which must not precede the specified first character.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



<b>GetCharWidth32</b> cannot be used on TrueType fonts. To retrieve character widths for TrueType fonts, use <a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>.

The range is inclusive; that is, the returned widths include the widths of the characters specified by the <i>iFirstChar</i> and <i>iLastChar</i> parameters.

If a character does not exist in the current font, it is assigned the width of the default character.


#### Examples

For an example, see "Displaying Keyboard Input" in <a href="_win32_Using_Keyboard_Input_cpp">Using Keyboard Input</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>



<a href="https://msdn.microsoft.com/552942c9-e2a6-43f9-901f-3aba1e2523e5">GetCharABCWidthsFloat</a>



<a href="https://msdn.microsoft.com/7a90b701-63f9-41e5-9069-10d344edfe02">GetCharWidthFloat</a>
 

 

