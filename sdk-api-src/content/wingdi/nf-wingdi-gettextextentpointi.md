---
UID: NF:wingdi.GetTextExtentPointI
title: GetTextExtentPointI function
author: windows-sdk-content
description: The GetTextExtentPointI function computes the width and height of the specified array of glyph indices.
old-location: gdi\gettextextentpointi.htm
tech.root: gdi
ms.assetid: d06a48dd-3f38-4c60-a4c6-954e43f718d1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTextExtentPointI, GetTextExtentPointI function [Windows GDI], _win32_GetTextExtentPointI, gdi.gettextextentpointi, wingdi/GetTextExtentPointI
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetTextExtentPointI
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTextExtentPointI function


## -description


The <b>GetTextExtentPointI</b> function computes the width and height of the specified array of glyph indices.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param pgiIn [in]

Pointer to array of glyph indices.


### -param cgi [in]

Specifies the number of glyph indices.


### -param psize [out]

Pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the dimensions of the string, in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>GetTextExtentPointI</b> function uses the currently selected font to compute the dimensions of the array of glyph indices. The width and height, in logical units, are computed without considering any clipping.

When this function returns the text extent, it assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if you use a font that specifies a nonzero escapement, this function doesn't use the angle while it computes the text extent. The app must convert it explicitly. However, when the graphics mode is set to <a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">GM_ADVANCED</a> and the character orientation is 90 degrees from the print orientation, the values that this function return do not follow this rule. When the character orientation and the print orientation match for a given string, this function returns the dimensions of the string in the <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure as { cx : 116, cy : 18 }.  When the character orientation and the print orientation are 90 degrees apart for the same string, this function returns the dimensions of the string in the <b>SIZE</b> structure as { cx : 18, cy : 116 }.

Because some devices kern characters, the sum of the extents of the individual glyph indices may not be equal to the extent of the entire array of glyph indices.

The calculated string width takes into account the intercharacter spacing set by the <a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a> function.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/731085ce-009d-42e1-885f-2f5151e0f6d3">GetTextExtentPoint</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>



<a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a>
 

 

