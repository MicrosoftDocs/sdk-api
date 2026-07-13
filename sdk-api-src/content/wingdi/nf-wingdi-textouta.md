---
UID: NF:wingdi.TextOutA
title: TextOutA function (wingdi.h)
description: The TextOut function writes a character string at the specified location, using the currently selected font, background color, and text color. (ANSI)
helpviewer_keywords: ["TextOutA", "wingdi/TextOutA"]
old-location: gdi\textout.htm
tech.root: gdi
ms.assetid: 0c437ff8-3893-4dc3-827b-fa9ce4bcd7e6
ms.date: 12/05/2018
ms.keywords: TextOut, TextOut function [Windows GDI], TextOutA, TextOutW, _win32_TextOut, gdi.textout, wingdi/TextOut, wingdi/TextOutA, wingdi/TextOutW
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TextOutW (Unicode) and TextOutA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TextOutA
 - wingdi/TextOutA
dev_langs:
 - c++
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
 - TextOut
 - TextOutA
 - TextOutW
---

# TextOutA function


## -description

The <b>TextOut</b> function writes a character string at the specified location, using the currently selected font, background color, and text color.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param x [in]

The x-coordinate, in logical coordinates, of the reference point that the system uses to align the string.

### -param y [in]

The y-coordinate, in logical coordinates, of the reference point that the system uses to align the string.

### -param lpString [in]

A pointer to the string to be drawn. The string does not need to be zero-terminated, because <i>cchString</i> specifies the length of the string.

### -param c [in]

The <a href="/windows/desktop/gdi/specifying-length-of-text-output-string">length of the string</a> pointed to by <i>lpString</i>, in characters.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The interpretation of the reference point depends on the current text-alignment mode. An application can retrieve this mode by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a> function; an application can alter this mode by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a> function. You can use the following values for text alignment. Only one flag can be chosen from those that affect horizontal and vertical alignment. In addition, only one of the two flags that alter the current position can be chosen.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="TA_BASELINE"></a><a id="ta_baseline"></a>TA_BASELINE

</td>
<td width="60%">
The reference point will be on the base line of the text.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_BOTTOM"></a><a id="ta_bottom"></a>TA_BOTTOM

</td>
<td width="60%">
The reference point will be on the bottom edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_TOP"></a><a id="ta_top"></a>TA_TOP

</td>
<td width="60%">
The reference point will be on the top edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_CENTER"></a><a id="ta_center"></a>TA_CENTER

</td>
<td width="60%">
The reference point will be aligned horizontally with the center of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_LEFT"></a><a id="ta_left"></a>TA_LEFT

</td>
<td width="60%">
The reference point will be on the left edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_RIGHT"></a><a id="ta_right"></a>TA_RIGHT

</td>
<td width="60%">
The reference point will be on the right edge of the bounding rectangle.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_NOUPDATECP"></a><a id="ta_noupdatecp"></a>TA_NOUPDATECP

</td>
<td width="60%">
The current position is not updated after each text output call. The reference point is passed to the text output function.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_RTLREADING"></a><a id="ta_rtlreading"></a>TA_RTLREADING

</td>
<td width="60%">
<b>Middle East language edition of Windows:</b> The text is laid out in right to left reading order, as opposed to the default left to right order. This applies only when the font selected into the device context is either Hebrew or Arabic.

</td>
</tr>
<tr>
<td width="40%">
<a id="TA_UPDATECP"></a><a id="ta_updatecp"></a>TA_UPDATECP

</td>
<td width="60%">
The current position is updated after each text output call. The current position is used as the reference point.

</td>
</tr>
</table>
 

By default, the current position is not used or updated by this function. However, an application can call the <a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a> function with the <i>fMode</i> parameter set to TA_UPDATECP to permit the system to use and update the current position each time the application calls <b>TextOut</b> for a specified device context. When this flag is set, the system ignores the <i>nXStart</i> and <i>nYStart</i> parameters on subsequent <b>TextOut</b> calls.

When the <b>TextOut</b> function is placed inside a path bracket, the system generates a path for the TrueType text that includes each character plus its character box. The region generated is the character box minus the text, rather than the text itself. You can obtain the region enclosed by the outline of the TrueType text by setting the background mode to transparent before placing the <b>TextOut</b> function in the path bracket. Following is sample code that demonstrates this procedure.


```cpp

// Obtain the window's client rectangle 
GetClientRect(hwnd, &r);

// THE FIX: by setting the background mode 
// to transparent, the region is the text itself 
// SetBkMode(hdc, TRANSPARENT); 

// Bracket begin a path 
BeginPath(hdc);

// Send some text out into the world 
TCHAR text[ ] = "Defenestration can be hazardous";
TextOut(hdc,r.left,r.top,text, ARRAYSIZE(text));

// Bracket end a path 
EndPath(hdc);

// Derive a region from that path 
SelectClipPath(hdc, RGN_AND);

// This generates the same result as SelectClipPath() 
// SelectClipRgn(hdc, PathToRegion(hdc)); 

// Fill the region with grayness 
FillRect(hdc, &r, GetStockObject(GRAY_BRUSH));

```



#### Examples

For an example, see <a href="/windows/desktop/gdi/enumerating-the-installed-fonts">Enumerating the Installed Fonts</a>.

<div class="code"></div>




> [!NOTE]
> The wingdi.h header defines TextOut as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-gettextalign">GetTextAlign</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor">SetBkColor</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextalign">SetTextAlign</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-settextcolor">SetTextColor</a>



<a href="/windows/desktop/api/winuser/nf-winuser-tabbedtextouta">TabbedTextOut</a>
