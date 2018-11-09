---
UID: NF:wingdi.GetTextExtentExPointA
title: GetTextExtentExPointA function
author: windows-sdk-content
description: The GetTextExtentExPoint function retrieves the number of characters in a specified string that will fit within a specified space and fills an array with the text extent for each of those characters.
old-location: gdi\gettextextentexpoint.htm
tech.root: gdi
ms.assetid: b873a059-5aa3-47d0-b109-7acd542c7d79
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetTextExtentExPoint, GetTextExtentExPoint function [Windows GDI], GetTextExtentExPointA, GetTextExtentExPointW, _win32_GetTextExtentExPoint, gdi.gettextextentexpoint, wingdi/GetTextExtentExPoint, wingdi/GetTextExtentExPointA, wingdi/GetTextExtentExPointW
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
req.unicode-ansi: GetTextExtentExPointW (Unicode) and GetTextExtentExPointA (ANSI)
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
 - GetTextExtentExPoint
 - GetTextExtentExPointA
 - GetTextExtentExPointW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTextExtentExPointA function


## -description


The <b>GetTextExtentExPoint</b> function retrieves the number of characters in a specified string that will fit within a specified space and fills an array with the text extent for each of those characters. (A text extent is the distance between the beginning of the space and a character that will fit in the space.) This information is useful for word-wrapping calculations.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpszString [in]

A pointer to the null-terminated string for which extents are to be retrieved.


### -param cchString [in]

The number of characters in the string pointed to by the <i>lpszStr</i> parameter. For an ANSI call it specifies the string length in bytes and for a Unicode it specifies the string length in WORDs. Note that for the ANSI function, characters in SBCS code pages take one byte each, while most characters in DBCS code pages take two bytes; for the Unicode function, most currently defined Unicode characters (those in the Basic Multilingual Plane (BMP)) are one WORD while Unicode surrogates are two WORDs.


### -param nMaxExtent [in]

The maximum allowable width, in logical units, of the formatted string.


### -param lpnFit [out]

A pointer to an integer that receives a count of the maximum number of characters that will fit in the space specified by the <i>nMaxExtent</i> parameter. When the <i>lpnFit</i> parameter is <b>NULL</b>, the <i>nMaxExtent</i> parameter is ignored.


### -param lpnDx [out]

A pointer to an array of integers that receives partial string extents. Each element in the array gives the distance, in logical units, between the beginning of the string and one of the characters that fits in the space specified by the <i>nMaxExtent</i> parameter. This array must have at least as many elements as characters specified by the <i>cchString</i> parameter because the entire array is used internally. The function fills the array with valid extents for as many characters as are specified by the <i>lpnFit</i> parameter. Any values in the rest of the array should be ignored. If <i>alpDx</i> is <b>NULL</b>, the function does not compute partial string widths.

For complex scripts, where a sequence of characters may be represented by any number of glyphs, the values in the <i>alpDx</i> array up to the number specified by the <i>lpnFit</i> parameter match one-to-one with code points. Again, you should ignore the rest of the values in the <i>alpDx</i> array.


### -param lpSize [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the dimensions of the string, in logical units. This parameter cannot be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If both the <i>lpnFit</i> and <i>alpDx</i> parameters are <b>NULL</b>, calling the <b>GetTextExtentExPoint</b> function is equivalent to calling the <a href="https://msdn.microsoft.com/731085ce-009d-42e1-885f-2f5151e0f6d3">GetTextExtentPoint</a> function.

For the ANSI version of <b>GetTextExtentExPoint</b>, the <i>lpDx</i> array has the same number of INT values as there are bytes in <i>lpString</i>. The INT values that correspond to the two bytes of a DBCS character are each the extent of the entire composite character.

Note, the <i>alpDx</i> values for <b>GetTextExtentExPoint</b> are not the same as the <i>lpDx</i> values for <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>. To use the <i>alpDx</i> values in <i>lpDx</i>, you must first process them.

When this function returns the text extent, it assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if you use a font that specifies a nonzero escapement, this function doesn't use the angle while it computes the text extent. The app must convert it explicitly. However, when the graphics mode is set to <a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">GM_ADVANCED</a> and the character orientation is 90 degrees from the print orientation, the values that this function return do not follow this rule. When the character orientation and the print orientation match for a given string, this function returns the dimensions of the string in the <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure as { cx : 116, cy : 18 }.  When the character orientation and the print orientation are 90 degrees apart for the same string, this function returns the dimensions of the string in the <b>SIZE</b> structure as { cx : 18, cy : 116 }.

This function returns the extent of each successive character in a string. When these are rounded to logical units, you get different results than what is returned from the <a href="https://msdn.microsoft.com/be29c195-cf67-45d5-8a46-ac572afb756d">GetCharWidth</a>, which returns the width of each individual character rounded to logical units.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/731085ce-009d-42e1-885f-2f5151e0f6d3">GetTextExtentPoint</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

