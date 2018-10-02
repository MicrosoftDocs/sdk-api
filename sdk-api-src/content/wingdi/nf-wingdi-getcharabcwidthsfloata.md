---
UID: NF:wingdi.GetCharABCWidthsFloatA
title: GetCharABCWidthsFloatA function
author: windows-sdk-content
description: The GetCharABCWidthsFloat function retrieves the widths, in logical units, of consecutive characters in a specified range from the current font.
old-location: gdi\getcharabcwidthsfloat.htm
tech.root: gdi
ms.assetid: 552942c9-e2a6-43f9-901f-3aba1e2523e5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCharABCWidthsFloat, GetCharABCWidthsFloat function [Windows GDI], GetCharABCWidthsFloatA, GetCharABCWidthsFloatW, _win32_GetCharABCWidthsFloat, gdi.getcharabcwidthsfloat, wingdi/GetCharABCWidthsFloat, wingdi/GetCharABCWidthsFloatA, wingdi/GetCharABCWidthsFloatW
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
req.unicode-ansi: GetCharABCWidthsFloatW (Unicode) and GetCharABCWidthsFloatA (ANSI)
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
 - GetCharABCWidthsFloat
 - GetCharABCWidthsFloatA
 - GetCharABCWidthsFloatW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCharABCWidthsFloatA function


## -description


The <b>GetCharABCWidthsFloat</b> function retrieves the widths, in logical units, of consecutive characters in a specified range from the current font.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param iFirst [in]

Specifies the code point of the first character in the group of consecutive characters where the ABC widths are seeked.


### -param iLast [in]

Specifies the code point of the last character in the group of consecutive characters where the ABC widths are seeked. This range is inclusive. An error is returned if the specified last character precedes the specified first character.


### -param lpABC [out]

Pointer to an array of <a href="https://msdn.microsoft.com/540bb00c-f0e2-4ddd-98d1-cf3ed86b6ce0">ABCFLOAT</a> structures that receives the character widths, in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Unlike the <a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a> function that returns widths only for TrueType fonts, the <b>GetCharABCWidthsFloat</b> function retrieves widths for any font. The widths returned by this function are in the IEEE floating-point format.

If the current world-to-device transformation is not identified, the returned widths may be noninteger values, even if the corresponding values in the device space are integers.

A spacing is the distance added to the current position before placing the glyph. B spacing is the width of the black part of the glyph. C spacing is the distance added to the current position to provide white space to the right of the glyph. The total advanced width is specified by A+B+C.

The ABC spaces are measured along the character base line of the selected font.

The ABC widths of the default character are used for characters outside the range of the currently selected font.




## -see-also




<a href="https://msdn.microsoft.com/540bb00c-f0e2-4ddd-98d1-cf3ed86b6ce0">ABCFLOAT</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/b48ab66d-ff0a-48d9-b7dd-28610bf69d51">GetCharABCWidths</a>



<a href="https://msdn.microsoft.com/be29c195-cf67-45d5-8a46-ac572afb756d">GetCharWidth</a>



<a href="https://msdn.microsoft.com/7a90b701-63f9-41e5-9069-10d344edfe02">GetCharWidthFloat</a>
 

 

