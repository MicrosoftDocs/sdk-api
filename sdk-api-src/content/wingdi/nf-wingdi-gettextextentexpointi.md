---
UID: NF:wingdi.GetTextExtentExPointI
title: GetTextExtentExPointI function
author: windows-sdk-content
description: The GetTextExtentExPointI function retrieves the number of characters in a specified string that will fit within a specified space and fills an array with the text extent for each of those characters.
old-location: gdi\gettextextentexpointi.htm
tech.root: gdi
ms.assetid: d543ec43-f6f1-4463-b27d-a1abf1cf3961
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTextExtentExPointI, GetTextExtentExPointI function [Windows GDI], _win32_GetTextExtentExPointI, gdi.gettextextentexpointi, wingdi/GetTextExtentExPointI
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
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetTextExtentExPointI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTextExtentExPointI function


## -description


The <b>GetTextExtentExPointI</b> function retrieves the number of characters in a specified string that will fit within a specified space and fills an array with the text extent for each of those characters. (A text extent is the distance between the beginning of the space and a character that will fit in the space.) This information is useful for word-wrapping calculations.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpwszString [in]

A pointer to an array of glyph indices for which extents are to be retrieved.


### -param cwchString [in]

The number of glyphs in the array pointed to by the <i>pgiIn</i> parameter.


### -param nMaxExtent [in]

The maximum allowable width, in logical units, of the formatted string.


### -param lpnFit [out]

A pointer to an integer that receives a count of the maximum number of characters that will fit in the space specified by the <i>nMaxExtent</i> parameter. When the <i>lpnFit</i> parameter is <b>NULL</b>, the <i>nMaxExtent</i> parameter is ignored.


### -param lpnDx [out]

A pointer to an array of integers that receives partial glyph extents. Each element in the array gives the distance, in logical units, between the beginning of the glyph indices array and one of the glyphs that fits in the space specified by the <i>nMaxExtent</i> parameter. Although this array should have at least as many elements as glyph indices specified by the <i>cgi</i> parameter, the function fills the array with extents only for as many glyph indices as are specified by the <i>lpnFit</i> parameter. If <i>lpnFit</i> is <b>NULL</b>, the function does not compute partial string widths.


### -param lpSize [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the dimensions of the glyph indices array, in logical units. This value cannot be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



If both the <i>lpnFit</i> and <i>alpDx</i> parameters are <b>NULL</b>, calling the <b>GetTextExtentExPointI</b> function is equivalent to calling the <a href="https://msdn.microsoft.com/d06a48dd-3f38-4c60-a4c6-954e43f718d1">GetTextExtentPointI</a> function.

When this function returns the text extent, it assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if you use a font that specifies a nonzero escapement, this function doesn't use the angle while it computes the text extent. The app must convert it explicitly. However, when the graphics mode is set to <a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">GM_ADVANCED</a> and the character orientation is 90 degrees from the print orientation, the values that this function return do not follow this rule. When the character orientation and the print orientation match for a given string, this function returns the dimensions of the string in the <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure as { cx : 116, cy : 18 }.  When the character orientation and the print orientation are 90 degrees apart for the same string, this function returns the dimensions of the string in the <b>SIZE</b> structure as { cx : 18, cy : 116 }.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/731085ce-009d-42e1-885f-2f5151e0f6d3">GetTextExtentPoint</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

