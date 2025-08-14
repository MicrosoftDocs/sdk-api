---
UID: NF:winuser.DrawTextW
title: DrawTextW function (winuser.h)
description: The DrawTextW (Unicode) function draws formatted text in the specified rectangle. (DrawTextW function)
helpviewer_keywords: ["DT_BOTTOM", "DT_CALCRECT", "DT_CENTER", "DT_EDITCONTROL", "DT_END_ELLIPSIS", "DT_EXPANDTABS", "DT_EXTERNALLEADING", "DT_HIDEPREFIX", "DT_INTERNAL", "DT_LEFT", "DT_MODIFYSTRING", "DT_NOCLIP", "DT_NOFULLWIDTHCHARBREAK", "DT_NOPREFIX", "DT_PATH_ELLIPSIS", "DT_PREFIXONLY", "DT_RIGHT", "DT_RTLREADING", "DT_SINGLELINE", "DT_TABSTOP", "DT_TOP", "DT_VCENTER", "DT_WORDBREAK", "DT_WORD_ELLIPSIS", "DrawText", "DrawText function [Windows GDI]", "DrawTextW", "_win32_DrawText", "gdi.drawtext", "winuser/DrawText", "winuser/DrawTextW"]

old-location: gdi\drawtext.htm
tech.root: gdi
ms.assetid: fe412280-d797-4abd-8a29-107a9cd96145
ms.date: 08/02/2022
ms.keywords: DT_BOTTOM, DT_CALCRECT, DT_CENTER, DT_EDITCONTROL, DT_END_ELLIPSIS, DT_EXPANDTABS, DT_EXTERNALLEADING, DT_HIDEPREFIX, DT_INTERNAL, DT_LEFT, DT_MODIFYSTRING, DT_NOCLIP, DT_NOFULLWIDTHCHARBREAK, DT_NOPREFIX, DT_PATH_ELLIPSIS, DT_PREFIXONLY, DT_RIGHT, DT_RTLREADING, DT_SINGLELINE, DT_TABSTOP, DT_TOP, DT_VCENTER, DT_WORDBREAK, DT_WORD_ELLIPSIS, DrawText, DrawText function [Windows GDI], DrawTextA, DrawTextW, _win32_DrawText, gdi.drawtext, winuser/DrawText, winuser/DrawTextA, winuser/DrawTextW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DrawTextW (Unicode) and DrawTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawTextW
 - winuser/DrawTextW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - user32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - DrawText
 - DrawTextA
 - DrawTextW
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# DrawTextW function


## -description

The <b>DrawText</b> function draws formatted text in the specified rectangle. It formats the text according to the specified method (expanding tabs, justifying characters, breaking lines, and so forth).

To specify additional formatting options, use the <a href="/windows/desktop/api/winuser/nf-winuser-drawtextexa">DrawTextEx</a> function.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param lpchText [in, out]

A pointer to the string that specifies the text to be drawn. If the <i>nCount</i> parameter is -1, the string must be null-terminated.

If <i>uFormat</i> includes DT_MODIFYSTRING, the function could add up to four additional characters to this string. The buffer containing the string should be large enough to accommodate these extra characters.

### -param cchText [in]

The length, in characters, of the string. If <i>nCount</i> is -1, then the <i>lpchText</i> parameter is assumed to be a pointer to a null-terminated string and <b>DrawText</b> computes the character count automatically.

### -param lprc [in, out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the rectangle (in logical coordinates) in which the text is to be formatted.

### -param format [in]

The method of formatting the text. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DT_BOTTOM"></a><a id="dt_bottom"></a><dl>
<dt><b>DT_BOTTOM</b></dt>
</dl>
</td>
<td width="60%">
Justifies the text to the bottom of the rectangle. This value is used only with the DT_SINGLELINE value.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_CALCRECT"></a><a id="dt_calcrect"></a><dl>
<dt><b>DT_CALCRECT</b></dt>
</dl>
</td>
<td width="60%">
Determines the width and height of the rectangle. If there are multiple lines of text, <b>DrawText</b> uses the width of the rectangle pointed to by the <i>lpRect</i> parameter and extends the base of the rectangle to bound the last line of text. If the largest word is wider than the rectangle, the width is expanded. If the text is less than the width of the rectangle, the width is reduced. If there is only one line of text, <b>DrawText</b> modifies the right side of the rectangle so that it bounds the last character in the line. In either case, <b>DrawText</b> returns the height of the formatted text but does not draw the text.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_CENTER"></a><a id="dt_center"></a><dl>
<dt><b>DT_CENTER</b></dt>
</dl>
</td>
<td width="60%">
Centers text horizontally in the rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_EDITCONTROL"></a><a id="dt_editcontrol"></a><dl>
<dt><b>DT_EDITCONTROL</b></dt>
</dl>
</td>
<td width="60%">
Duplicates the text-displaying characteristics of a multiline edit control. Specifically, the average character width is calculated in the same manner as for an edit control, and the function does not display a partially visible last line.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_END_ELLIPSIS"></a><a id="dt_end_ellipsis"></a><dl>
<dt><b>DT_END_ELLIPSIS</b></dt>
</dl>
</td>
<td width="60%">
For displayed text, if the end of a string does not fit in the rectangle, it is truncated and ellipses are added. If a word that is not at the end of the string goes beyond the limits of the rectangle, it is truncated without ellipses.

The string is not modified unless the DT_MODIFYSTRING flag is specified.

Compare with DT_PATH_ELLIPSIS and DT_WORD_ELLIPSIS.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_EXPANDTABS"></a><a id="dt_expandtabs"></a><dl>
<dt><b>DT_EXPANDTABS</b></dt>
</dl>
</td>
<td width="60%">
Expands tab characters. The default number of characters per tab is eight. The DT_WORD_ELLIPSIS, DT_PATH_ELLIPSIS, and DT_END_ELLIPSIS values cannot be used with the DT_EXPANDTABS value.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_EXTERNALLEADING"></a><a id="dt_externalleading"></a><dl>
<dt><b>DT_EXTERNALLEADING</b></dt>
</dl>
</td>
<td width="60%">
Includes the font external leading in line height. Normally, external leading is not included in the height of a line of text.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_HIDEPREFIX"></a><a id="dt_hideprefix"></a><dl>
<dt><b>DT_HIDEPREFIX</b></dt>
</dl>
</td>
<td width="60%">
Ignores the ampersand (&amp;) prefix character in the text. The letter that follows will not be underlined, but other mnemonic-prefix characters are still processed.

Example:

input string: "A&amp;bc&amp;&amp;d"

normal: "A<u>b</u>c&amp;d"

DT_HIDEPREFIX: "Abc&amp;d"

Compare with DT_NOPREFIX and DT_PREFIXONLY.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_INTERNAL"></a><a id="dt_internal"></a><dl>
<dt><b>DT_INTERNAL</b></dt>
</dl>
</td>
<td width="60%">
Uses the system font to calculate text metrics.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_LEFT"></a><a id="dt_left"></a><dl>
<dt><b>DT_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Aligns text to the left.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_MODIFYSTRING"></a><a id="dt_modifystring"></a><dl>
<dt><b>DT_MODIFYSTRING</b></dt>
</dl>
</td>
<td width="60%">
Modifies the specified string to match the displayed text. This value has no effect unless DT_END_ELLIPSIS or DT_PATH_ELLIPSIS is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_NOCLIP"></a><a id="dt_noclip"></a><dl>
<dt><b>DT_NOCLIP</b></dt>
</dl>
</td>
<td width="60%">
Draws without clipping. <b>DrawText</b> is somewhat faster when DT_NOCLIP is used.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_NOFULLWIDTHCHARBREAK"></a><a id="dt_nofullwidthcharbreak"></a><dl>
<dt><b>DT_NOFULLWIDTHCHARBREAK</b></dt>
</dl>
</td>
<td width="60%">
Prevents a line break at a DBCS (double-wide character string), so that the line breaking rule is equivalent to SBCS strings. For example, this can be used in Korean windows, for more readability of icon labels. This value has no effect unless DT_WORDBREAK is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_NOPREFIX"></a><a id="dt_noprefix"></a><dl>
<dt><b>DT_NOPREFIX</b></dt>
</dl>
</td>
<td width="60%">
Turns off processing of prefix characters. Normally, <b>DrawText</b> interprets the mnemonic-prefix character &amp; as a directive to underscore the character that follows, and the mnemonic-prefix characters &amp;&amp; as a directive to print a single &amp;. By specifying DT_NOPREFIX, this processing is turned off. For example,

Example:

input string: "A&amp;bc&amp;&amp;d"

normal: "A<u>b</u>c&amp;d"

DT_NOPREFIX: "A&amp;bc&amp;&amp;d"

Compare with DT_HIDEPREFIX and DT_PREFIXONLY.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_PATH_ELLIPSIS"></a><a id="dt_path_ellipsis"></a><dl>
<dt><b>DT_PATH_ELLIPSIS</b></dt>
</dl>
</td>
<td width="60%">
For displayed text, replaces characters in the middle of the string with ellipses so that the result fits in the specified rectangle. If the string contains backslash (\\) characters, DT_PATH_ELLIPSIS preserves as much as possible of the text after the last backslash.

The string is not modified unless the DT_MODIFYSTRING flag is specified.

Compare with DT_END_ELLIPSIS and DT_WORD_ELLIPSIS.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_PREFIXONLY"></a><a id="dt_prefixonly"></a><dl>
<dt><b>DT_PREFIXONLY</b></dt>
</dl>
</td>
<td width="60%">
Draws only an underline at the position of the character following the ampersand (&amp;) prefix character. Does not draw any other characters in the string. For example,

Example:

input string: "A&amp;bc&amp;&amp;d"n

normal: "A<u>b</u>c&amp;d"

DT_PREFIXONLY: " _    "

Compare with DT_HIDEPREFIX and DT_NOPREFIX.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_RIGHT"></a><a id="dt_right"></a><dl>
<dt><b>DT_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Aligns text to the right.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_RTLREADING"></a><a id="dt_rtlreading"></a><dl>
<dt><b>DT_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
Layout in right-to-left reading order for bidirectional text when the font selected into the <i>hdc</i> is a Hebrew or Arabic font. The default reading order for all text is left-to-right.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_SINGLELINE"></a><a id="dt_singleline"></a><dl>
<dt><b>DT_SINGLELINE</b></dt>
</dl>
</td>
<td width="60%">
Displays text on a single line only. Carriage returns and line feeds do not break the line.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_TABSTOP"></a><a id="dt_tabstop"></a><dl>
<dt><b>DT_TABSTOP</b></dt>
</dl>
</td>
<td width="60%">
Sets tab stops. Bits 15-8 (high-order byte of the low-order word) of the <i>uFormat</i> parameter specify the number of characters for each tab. The default number of characters per tab is eight. The DT_CALCRECT, DT_EXTERNALLEADING, DT_INTERNAL, DT_NOCLIP, and DT_NOPREFIX values cannot be used with the DT_TABSTOP value.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_TOP"></a><a id="dt_top"></a><dl>
<dt><b>DT_TOP</b></dt>
</dl>
</td>
<td width="60%">
Justifies the text to the top of the rectangle.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_VCENTER"></a><a id="dt_vcenter"></a><dl>
<dt><b>DT_VCENTER</b></dt>
</dl>
</td>
<td width="60%">
Centers text vertically. This value is used only with the DT_SINGLELINE value.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_WORDBREAK"></a><a id="dt_wordbreak"></a><dl>
<dt><b>DT_WORDBREAK</b></dt>
</dl>
</td>
<td width="60%">
Breaks words. Lines are automatically broken between words if a word would extend past the edge of the rectangle specified by the <i>lpRect</i> parameter. A carriage return-line feed sequence also breaks the line.

If this is not specified, output is on one line.

</td>
</tr>
<tr>
<td width="40%"><a id="DT_WORD_ELLIPSIS"></a><a id="dt_word_ellipsis"></a><dl>
<dt><b>DT_WORD_ELLIPSIS</b></dt>
</dl>
</td>
<td width="60%">
Truncates any word that does not fit in the rectangle and adds ellipses.

Compare with DT_END_ELLIPSIS and DT_PATH_ELLIPSIS.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the height of the text in logical units. If DT_VCENTER or DT_BOTTOM is specified, the return value is the offset from <code>lpRect-&gt;top</code> to the bottom of the drawn text

If the function fails, the return value is zero.

## -remarks

The <b>DrawText</b> function uses the device context's selected font, text color, and background color to draw the text. Unless the DT_NOCLIP format is used, <b>DrawText</b> clips the text so that it does not appear outside the specified rectangle. Note that text with significant overhang may be clipped, for example, an initial "W" in the text string or text that is in italics. All formatting is assumed to have multiple lines unless the DT_SINGLELINE format is specified.

If the selected font is too large for the specified rectangle, the <b>DrawText</b> function does not attempt to substitute a smaller font.

The text alignment mode for the device context must include the TA_LEFT, TA_TOP, and TA_NOUPDATECP flags.





> [!NOTE]
> The winuser.h header defines DrawText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-drawtextexa">DrawTextEx
      </a>



<a href="/windows/desktop/gdi/font-and-text-functions">Font and Text Functions</a>



<a href="/windows/desktop/gdi/fonts-and-text">Fonts and Text Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-graystringa">GrayString
      </a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT
      </a>



<a href="/windows/desktop/api/winuser/nf-winuser-tabbedtextouta">TabbedTextOut
      </a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-textouta">TextOut
      </a>
