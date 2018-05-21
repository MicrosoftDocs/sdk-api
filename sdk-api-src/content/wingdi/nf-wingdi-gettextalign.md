---
UID: NF:wingdi.GetTextAlign
title: GetTextAlign function
author: windows-driver-content
description: The GetTextAlign function retrieves the text-alignment setting for the specified device context.
old-location: gdi\gettextalign.htm
old-project: gdi
ms.assetid: d3ec0350-2eb8-4843-88bb-d72cece710e7
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetTextAlign, GetTextAlign function [Windows GDI], _win32_GetTextAlign, gdi.gettextalign, wingdi/GetTextAlign
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
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
-	GDI32Full.dll
api_name:
-	GetTextAlign
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetTextAlign function


## -description


The <b>GetTextAlign</b> function retrieves the text-alignment setting for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value is the status of the text-alignment flags. For more information about the return value, see the Remarks section. The return value is a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TA_BASELINE</td>
<td>The reference point is on the base line of the text.</td>
</tr>
<tr>
<td>TA_BOTTOM</td>
<td>The reference point is on the bottom edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_TOP</td>
<td>The reference point is on the top edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_CENTER</td>
<td>The reference point is aligned horizontally with the center of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_LEFT</td>
<td>The reference point is on the left edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_RIGHT</td>
<td>The reference point is on the right edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_RTLREADING</td>
<td><b>Middle East language edition of Windows:</b> The text is laid out in right to left reading order, as opposed to the default left to right order. This only applies when the font selected into the device context is either Hebrew or Arabic.</td>
</tr>
<tr>
<td>TA_NOUPDATECP</td>
<td>The current position is not updated after each text output call.</td>
</tr>
<tr>
<td>TA_UPDATECP</td>
<td>The current position is updated after each text output call.</td>
</tr>
</table>
 

When the current font has a vertical default base line (as with Kanji), the following values are used instead of TA_BASELINE and TA_CENTER.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>VTA_BASELINE</td>
<td>The reference point is on the base line of the text.</td>
</tr>
<tr>
<td>VTA_CENTER</td>
<td>The reference point is aligned vertically with the center of the bounding rectangle.</td>
</tr>
</table>
 

If the function fails, the return value is GDI_ERROR.




## -remarks



The bounding rectangle is a rectangle bounding all of the character cells in a string of text. Its dimensions can be obtained by calling the <a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a> function.

The text-alignment flags determine how the <a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a> and <a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a> functions align a string of text in relation to the string's reference point provided to <b>TextOut</b> or <b>ExtTextOut</b>.

The text-alignment flags are not necessarily single bit flags and may be equal to zero. The flags must be examined in groups of related flags, as shown in the following list.

<ul>
<li>TA_LEFT, TA_RIGHT, and TA_CENTER</li>
<li>TA_BOTTOM, TA_TOP, and TA_BASELINE</li>
<li>TA_NOUPDATECP and TA_UPDATECP</li>
</ul>
If the current font has a vertical default base line, the related flags are as shown in the following list.

<ul>
<li>TA_LEFT, TA_RIGHT, and VTA_BASELINE</li>
<li>TA_BOTTOM, TA_TOP, and VTA_CENTER</li>
<li>TA_NOUPDATECP and TA_UPDATECP</li>
</ul>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To verify that a particular flag is set in the return value of this function:</b>

<ol>
<li>Apply the bitwise OR operator to the flag and its related flags.</li>
<li>Apply the bitwise AND operator to the result and the return value.</li>
<li>Test for the equality of this result and the flag.</li>
</ol>

#### Examples

For an example, see <a href="https://msdn.microsoft.com/7fdfbadb-827a-4b42-9b9a-b9e46389e13c">Setting the Text Alignment</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/74f8fcb8-8ad4-47f2-a330-fa56713bdb37">ExtTextOut</a>



<a href="https://msdn.microsoft.com/69c04ed7-52da-4cb6-9fd2-f2a8c044df8b">Font and Text Functions</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/530280ee-dfd8-4905-9b72-6c19efcff133">GetTextExtentPoint32</a>



<a href="https://msdn.microsoft.com/422868c5-14c9-4374-9cc5-b7bf91ab9eb4">SetTextAlign</a>



<a href="https://msdn.microsoft.com/0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6">TextOut</a>
 

 

