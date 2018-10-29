---
UID: NF:wingdi.GetCharABCWidthsW
title: GetCharABCWidthsW function
author: windows-sdk-content
description: The GetCharABCWidths function retrieves the widths, in logical units, of consecutive characters in a specified range from the current TrueType font. This function succeeds only with TrueType fonts.
old-location: gdi\getcharabcwidths.htm
tech.root: gdi
ms.assetid: b48ab66d-ff0a-48d9-b7dd-28610bf69d51
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetCharABCWidths, GetCharABCWidths function [Windows GDI], GetCharABCWidthsA, GetCharABCWidthsW, _win32_GetCharABCWidths, gdi.getcharabcwidths, wingdi/GetCharABCWidths, wingdi/GetCharABCWidthsA, wingdi/GetCharABCWidthsW
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
req.unicode-ansi: GetCharABCWidthsW (Unicode) and GetCharABCWidthsA (ANSI)
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
 - Ext-MS-Win-GDI-Font-l1-1-1.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetCharABCWidths
 - GetCharABCWidthsA
 - GetCharABCWidthsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCharABCWidthsW function


## -description


The <b>GetCharABCWidths</b> function retrieves the widths, in logical units, of consecutive characters in a specified range from the current TrueType font. This function succeeds only with TrueType fonts.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param wFirst [in]

The first character in the group of consecutive characters from the current font.


### -param wLast [in]

The last character in the group of consecutive characters from the current font.


### -param lpABC [out]

A pointer to an array of <a href="https://msdn.microsoft.com/00000000-0000-0000-0000-000000000001">ABC</a> structures that receives the character widths, in logical units. This array must contain at least as many <b>ABC</b> structures as there are characters in the range specified by the <i>uFirstChar</i> and <i>uLastChar</i> parameters.


## -returns



If the function succeeds, the return value is nonzero

If the function fails, the return value is zero.




## -remarks



The TrueType rasterizer provides ABC character spacing after a specific point size has been selected. A spacing is the distance added to the current position before placing the glyph. B spacing is the width of the black part of the glyph. C spacing is the distance added to the current position to provide white space to the right of the glyph. The total advanced width is specified by A+B+C.

When the <b>GetCharABCWidths</b> function retrieves negative A or C widths for a character, that character includes underhangs or overhangs.

To convert the ABC widths to font design units, an application should use the value stored in the <b>otmEMSquare</b> member of a <a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a> structure. This value can be retrieved by calling the <a href="https://msdn.microsoft.com/b8c7a557-ca35-41a4-9043-8496e5b01564">GetOutlineTextMetrics</a> function.

The ABC widths of the default character are used for characters outside the range of the currently selected font.

To retrieve the widths of characters in non-TrueType fonts, applications should use the <a href="https://msdn.microsoft.com/be29c195-cf67-45d5-8a46-ac572afb756d">GetCharWidth</a> function.




## -see-also




<a href="https://msdn.microsoft.com/00000000-0000-0000-0000-000000000001">ABC</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/be29c195-cf67-45d5-8a46-ac572afb756d">GetCharWidth</a>



<a href="https://msdn.microsoft.com/b8c7a557-ca35-41a4-9043-8496e5b01564">GetOutlineTextMetrics</a>



<a href="https://msdn.microsoft.com/79d77df0-193a-49a8-b93d-4ef5807c3c9b">OUTLINETEXTMETRIC</a>
 

 

