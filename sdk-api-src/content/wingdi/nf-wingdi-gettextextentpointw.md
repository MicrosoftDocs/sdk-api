---
UID: NF:wingdi.GetTextExtentPointW
title: GetTextExtentPointW function
author: windows-sdk-content
description: The GetTextExtentPoint function computes the width and height of the specified string of text.
old-location: gdi\gettextextentpoint.htm
tech.root: gdi
ms.assetid: 731085ce-009d-42e1-885f-2f5151e0f6d3
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetTextExtentPoint, GetTextExtentPoint function [Windows GDI], GetTextExtentPointA, GetTextExtentPointW, _win32_GetTextExtentPoint, gdi.gettextextentpoint, wingdi/GetTextExtentPoint, wingdi/GetTextExtentPointA, wingdi/GetTextExtentPointW
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
req.unicode-ansi: GetTextExtentPointW (Unicode) and GetTextExtentPointA (ANSI)
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
 - Gdi32.dll
 - ext-ms-win-gdi-font-l1-1-2.dll
 - Ext-MS-Win-GDI-Font-L1-1-3.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetTextExtentPoint
 - GetTextExtentPointA
 - GetTextExtentPointW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetTextExtentPointW function


## -description


The <b>GetTextExtentPoint</b> function computes the width and height of the specified string of text.


<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should call the <a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a> function, which provides more accurate results.</div>
<div> </div>



## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpString [in]

A pointer to the string that specifies the text. The string does not need to be zero-terminated, since <i>cbString</i> specifies the length of the string.


### -param c [in]

The <a href="https://msdn.microsoft.com/695fd0f9-abd4-4666-acad-2c409624ddc6">length of the string</a> pointed to by <i>lpString</i>.


### -param lpsz [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the dimensions of the string, in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>GetTextExtentPoint</b> function uses the currently selected font to compute the dimensions of the string. The width and height, in logical units, are computed without considering any clipping. Also, this function assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if using a font specifying a nonzero escapement, this function will not use the angle while computing the text extent. The application must convert it explicitly.

Because some devices kern characters, the sum of the extents of the characters in a string may not be equal to the extent of the string.

The calculated string width takes into account the intercharacter spacing set by the <a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a> function.




## -see-also




<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>



<a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a>
 

 

