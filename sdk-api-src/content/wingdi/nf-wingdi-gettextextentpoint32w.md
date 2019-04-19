---
UID: NF:wingdi.GetTextExtentPoint32W
title: GetTextExtentPoint32W function (wingdi.h)
author: windows-sdk-content
description: The GetTextExtentPoint32 function computes the width and height of the specified string of text.
old-location: gdi\gettextextentpoint32.htm
tech.root: gdi
ms.assetid: 530280ee-dfd8-4905-9b72-6c19efcff133
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTextExtentPoint32, GetTextExtentPoint32 function [Windows GDI], GetTextExtentPoint32A, GetTextExtentPoint32W, _win32_GetTextExtentPoint32, gdi.gettextextentpoint32, wingdi/GetTextExtentPoint32, wingdi/GetTextExtentPoint32A, wingdi/GetTextExtentPoint32W
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTextExtentPoint32W (Unicode) and GetTextExtentPoint32A (ANSI)
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
 - GetTextExtentPoint32
 - GetTextExtentPoint32A
 - GetTextExtentPoint32W
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTextExtentPoint32W function


## -description


The <b>GetTextExtentPoint32</b> function computes the width and height of the specified string of text.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpString [in]

A pointer to a buffer that specifies the text string. The string does not need to be null-terminated, because the <i>c</i> parameter specifies the length of the string.


### -param c [in]

The <a href="https://msdn.microsoft.com/695fd0f9-abd4-4666-acad-2c409624ddc6">length of the string</a> pointed to by <i>lpString</i>.


### -param psizl [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the dimensions of the string, in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>GetTextExtentPoint32</b> function uses the currently selected font to compute the dimensions of the string. The width and height, in logical units, are computed without considering any clipping.

Because some devices kern characters, the sum of the extents of the characters in a string may not be equal to the extent of the string.

The calculated string width takes into account the intercharacter spacing set by the <a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a> function and the justification set by <a href="https://msdn.microsoft.com/55fb5a28-b7da-40d8-8e64-4b42c23fa8b1">SetTextJustification</a>. This is true for both displaying on a screen and for printing. However, if <i>lpDx</i> is set in <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>, <b>GetTextExtentPoint32</b> does not take into account either intercharacter spacing or justification. In addition, for EMF, the print result always takes both intercharacter spacing and justification into account.

When dealing with text displayed on a screen, the calculated string width takes into account the intercharacter spacing set by the <a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a> function and the justification set by <a href="https://msdn.microsoft.com/55fb5a28-b7da-40d8-8e64-4b42c23fa8b1">SetTextJustification</a>. However, if <i>lpDx</i> is set in <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>, <b>GetTextExtentPoint32</b> does not take into account either intercharacter spacing or justification. However, when printing with EMF:

<ul>
<li>The print result ignores intercharacter spacing, although <b>GetTextExtentPoint32</b> takes it into account.</li>
<li>The print result takes justification into account, although <b>GetTextExtentPoint32</b> ignores it.</li>
</ul>
When this function returns the text extent, it assumes that the text is horizontal, that is, that the escapement is always 0. This is true for both the horizontal and vertical measurements of the text. Even if you use a font that specifies a nonzero escapement, this function doesn't use the angle while it computes the text extent. The app must convert it explicitly. However, when the graphics mode is set to <a href="https://msdn.microsoft.com/73824a14-2951-45a2-98cd-156418c59a2d">GM_ADVANCED</a> and the character orientation is 90 degrees from the print orientation, the values that this function return do not follow this rule. When the character orientation and the print orientation match for a given string, this function returns the dimensions of the string in the <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure as { cx : 116, cy : 18 }.  When the character orientation and the print orientation are 90 degrees apart for the same string, this function returns the dimensions of the string in the <b>SIZE</b> structure as { cx : 18, cy : 116 }.

<b>GetTextExtentPoint32</b> doesn't consider "\n" (new line) or "\r\n" (carriage return and new line) characters when it computes the height of a text string.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/d21613ef-1ba4-40bb-b922-afe287556441">Drawing Text from Different Fonts on the Same Line</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>



<a href="https://msdn.microsoft.com/83b7d225-4fb9-4c75-bc4a-e1bea7f901f1">SetTextCharacterExtra</a>



<a href="https://msdn.microsoft.com/55fb5a28-b7da-40d8-8e64-4b42c23fa8b1">SetTextJustification</a>
 

 

