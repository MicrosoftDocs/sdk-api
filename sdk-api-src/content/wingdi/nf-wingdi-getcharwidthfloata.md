---
UID: NF:wingdi.GetCharWidthFloatA
title: GetCharWidthFloatA function (wingdi.h)
description: The GetCharWidthFloat function retrieves the fractional widths of consecutive characters in a specified range from the current font.helpviewer_keywords: ["GetCharWidthFloat","GetCharWidthFloat function [Windows GDI]","GetCharWidthFloatA","GetCharWidthFloatW","_win32_GetCharWidthFloat","gdi.getcharwidthfloat","wingdi/GetCharWidthFloat","wingdi/GetCharWidthFloatA","wingdi/GetCharWidthFloatW"]
old-location: gdi\getcharwidthfloat.htm
tech.root: gdi
ms.assetid: 7a90b701-63f9-41e5-9069-10d344edfe02
ms.date: 12/05/2018
ms.keywords: GetCharWidthFloat, GetCharWidthFloat function [Windows GDI], GetCharWidthFloatA, GetCharWidthFloatW, _win32_GetCharWidthFloat, gdi.getcharwidthfloat, wingdi/GetCharWidthFloat, wingdi/GetCharWidthFloatA, wingdi/GetCharWidthFloatW
f1_keywords:
- wingdi/GetCharWidthFloat
dev_langs:
- c++
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
- GetCharWidthFloat
- GetCharWidthFloatA
- GetCharWidthFloatW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCharWidthFloatA function


## -description


The <b>GetCharWidthFloat</b> function retrieves the fractional widths of consecutive characters in a specified range from the current font.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param iFirst [in]

The code point of the first character in the group of consecutive characters.


### -param iLast [in]

The code point of the last character in the group of consecutive characters.


### -param lpBuffer [out]

A pointer to a buffer that receives the character widths, in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The returned widths are in the 32-bit IEEE floating-point format. (The widths are measured along the base line of the characters.)

If the <i>iFirstChar</i> parameter specifies the letter a and the <i>iLastChar</i> parameter specifies the letter z, <b>GetCharWidthFloat</b> retrieves the widths of all lowercase characters.

If a character does not exist in the current font, it is assigned the width of the default character.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsa">GetCharABCWidths</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getcharabcwidthsfloata">GetCharABCWidthsFloat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getcharwidth32a">GetCharWidth32</a>
 

 

