---
UID: NF:winbase.IsTextUnicode
title: IsTextUnicode function (winbase.h)
description: Determines if a buffer is likely to contain a form of Unicode text.
helpviewer_keywords: ["IS_TEXT_UNICODE_ASCII16","IS_TEXT_UNICODE_BUFFER_TOO_SMALL","IS_TEXT_UNICODE_CONTROLS","IS_TEXT_UNICODE_ILLEGAL_CHARS","IS_TEXT_UNICODE_NOT_ASCII_MASK","IS_TEXT_UNICODE_NOT_UNICODE_MASK","IS_TEXT_UNICODE_NULL_BYTES","IS_TEXT_UNICODE_ODD_LENGTH","IS_TEXT_UNICODE_REVERSE_ASCII16","IS_TEXT_UNICODE_REVERSE_CONTROLS","IS_TEXT_UNICODE_REVERSE_MASK","IS_TEXT_UNICODE_REVERSE_SIGNATURE","IS_TEXT_UNICODE_REVERSE_STATISTICS","IS_TEXT_UNICODE_SIGNATURE","IS_TEXT_UNICODE_STATISTICS","IS_TEXT_UNICODE_UNICODE_MASK","IsTextUnicode","IsTextUnicode function [Internationalization for Windows Applications]","_win32_IsTextUnicode","intl.istextunicode","winbase/IsTextUnicode"]
old-location: intl\istextunicode.htm
tech.root: Intl
ms.assetid: 47e05b5b-a16b-4957-bc86-ed3cef4968ee
ms.date: 12/05/2018
ms.keywords: IS_TEXT_UNICODE_ASCII16, IS_TEXT_UNICODE_BUFFER_TOO_SMALL, IS_TEXT_UNICODE_CONTROLS, IS_TEXT_UNICODE_ILLEGAL_CHARS, IS_TEXT_UNICODE_NOT_ASCII_MASK, IS_TEXT_UNICODE_NOT_UNICODE_MASK, IS_TEXT_UNICODE_NULL_BYTES, IS_TEXT_UNICODE_ODD_LENGTH, IS_TEXT_UNICODE_REVERSE_ASCII16, IS_TEXT_UNICODE_REVERSE_CONTROLS, IS_TEXT_UNICODE_REVERSE_MASK, IS_TEXT_UNICODE_REVERSE_SIGNATURE, IS_TEXT_UNICODE_REVERSE_STATISTICS, IS_TEXT_UNICODE_SIGNATURE, IS_TEXT_UNICODE_STATISTICS, IS_TEXT_UNICODE_UNICODE_MASK, IsTextUnicode, IsTextUnicode function [Internationalization for Windows Applications], _win32_IsTextUnicode, intl.istextunicode, winbase/IsTextUnicode
req.header: winbase.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsTextUnicode
 - winbase/IsTextUnicode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-base-util-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - IsTextUnicode
---

# IsTextUnicode function


## -description

Determines if a buffer is likely to contain a form of Unicode text.

## -parameters

### -param lpv [in]

Pointer to the input buffer to examine.

### -param iSize [in]

Size, in bytes, of the input buffer indicated by <i>lpv</i>.

### -param lpiResult [in, out, optional]

On input, pointer to the tests to apply to the input buffer text. On output, this parameter receives the results of the specified tests: 1 if the contents of the buffer pass a test, 0 for failure. Only flags that are set upon input to the function are significant upon output.

If <i>lpiResult</i> is <b>NULL</b>, the function uses all available tests to determine if the data in the buffer is likely to be Unicode text.

This parameter can be one or more of the following values. Values can be combined with binary "OR".

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_ASCII16"></a><a id="is_text_unicode_ascii16"></a><dl>
<dt><b>IS_TEXT_UNICODE_ASCII16</b></dt>
</dl>
</td>
<td width="60%">
The text is Unicode, and contains only zero-extended ASCII values/characters.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_REVERSE_ASCII16"></a><a id="is_text_unicode_reverse_ascii16"></a><dl>
<dt><b>IS_TEXT_UNICODE_REVERSE_ASCII16</b></dt>
</dl>
</td>
<td width="60%">
Same as the preceding, except that the Unicode text is byte-reversed.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_STATISTICS"></a><a id="is_text_unicode_statistics"></a><dl>
<dt><b>IS_TEXT_UNICODE_STATISTICS</b></dt>
</dl>
</td>
<td width="60%">
The text is probably Unicode, with the determination made by applying statistical analysis. Absolute certainty is not guaranteed. See the Remarks section.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_REVERSE_STATISTICS"></a><a id="is_text_unicode_reverse_statistics"></a><dl>
<dt><b>IS_TEXT_UNICODE_REVERSE_STATISTICS</b></dt>
</dl>
</td>
<td width="60%">
Same as the preceding, except that the text that is probably Unicode is byte-reversed.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_CONTROLS"></a><a id="is_text_unicode_controls"></a><dl>
<dt><b>IS_TEXT_UNICODE_CONTROLS</b></dt>
</dl>
</td>
<td width="60%">
The text contains Unicode representations of one or more of these nonprinting characters: RETURN, LINEFEED, SPACE, CJK_SPACE, TAB.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_REVERSE_CONTROLS"></a><a id="is_text_unicode_reverse_controls"></a><dl>
<dt><b>IS_TEXT_UNICODE_REVERSE_CONTROLS</b></dt>
</dl>
</td>
<td width="60%">
Same as the preceding, except that the Unicode characters are byte-reversed.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_BUFFER_TOO_SMALL"></a><a id="is_text_unicode_buffer_too_small"></a><dl>
<dt><b>IS_TEXT_UNICODE_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
There are too few characters in the buffer for meaningful analysis (fewer than two bytes).

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_SIGNATURE"></a><a id="is_text_unicode_signature"></a><dl>
<dt><b>IS_TEXT_UNICODE_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The text contains the Unicode byte-order mark (BOM) 0xFEFF as its first character.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_REVERSE_SIGNATURE"></a><a id="is_text_unicode_reverse_signature"></a><dl>
<dt><b>IS_TEXT_UNICODE_REVERSE_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
The text contains the Unicode byte-reversed byte-order mark (Reverse BOM) 0xFFFE as its first character.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_ILLEGAL_CHARS"></a><a id="is_text_unicode_illegal_chars"></a><dl>
<dt><b>IS_TEXT_UNICODE_ILLEGAL_CHARS</b></dt>
</dl>
</td>
<td width="60%">
The text contains one of these Unicode-illegal characters: embedded Reverse BOM, UNICODE_NUL, CRLF (packed into one word), or 0xFFFF.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_ODD_LENGTH"></a><a id="is_text_unicode_odd_length"></a><dl>
<dt><b>IS_TEXT_UNICODE_ODD_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
The number of characters in the string is odd. A string of odd length cannot (by definition) be Unicode text.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_NULL_BYTES"></a><a id="is_text_unicode_null_bytes"></a><dl>
<dt><b>IS_TEXT_UNICODE_NULL_BYTES</b></dt>
</dl>
</td>
<td width="60%">
The text contains null bytes, which indicate non-ASCII text.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_UNICODE_MASK"></a><a id="is_text_unicode_unicode_mask"></a><dl>
<dt><b>IS_TEXT_UNICODE_UNICODE_MASK</b></dt>
</dl>
</td>
<td width="60%">
The value is a combination of IS_TEXT_UNICODE_ASCII16, IS_TEXT_UNICODE_STATISTICS, IS_TEXT_UNICODE_CONTROLS, IS_TEXT_UNICODE_SIGNATURE.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_REVERSE_MASK"></a><a id="is_text_unicode_reverse_mask"></a><dl>
<dt><b>IS_TEXT_UNICODE_REVERSE_MASK</b></dt>
</dl>
</td>
<td width="60%">
The value is a combination of IS_TEXT_UNICODE_REVERSE_ASCII16, IS_TEXT_UNICODE_REVERSE_STATISTICS, IS_TEXT_UNICODE_REVERSE_CONTROLS, IS_TEXT_UNICODE_REVERSE_SIGNATURE.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_NOT_UNICODE_MASK"></a><a id="is_text_unicode_not_unicode_mask"></a><dl>
<dt><b>IS_TEXT_UNICODE_NOT_UNICODE_MASK</b></dt>
</dl>
</td>
<td width="60%">
The value is a combination of IS_TEXT_UNICODE_ILLEGAL_CHARS, IS_TEXT_UNICODE_ODD_LENGTH, and two currently unused bit flags.

</td>
</tr>
<tr>
<td width="40%"><a id="IS_TEXT_UNICODE_NOT_ASCII_MASK"></a><a id="is_text_unicode_not_ascii_mask"></a><dl>
<dt><b>IS_TEXT_UNICODE_NOT_ASCII_MASK</b></dt>
</dl>
</td>
<td width="60%">
The value is a combination of IS_TEXT_UNICODE_NULL_BYTES and three currently unused bit flags.

</td>
</tr>
</table>

## -returns

Returns a nonzero value if the data in the buffer passes the specified tests. The function returns 0 if the data in the buffer does not pass the specified tests.

## -remarks

This function uses various statistical and deterministic methods to make its determination, under the control of flags passed in the <i>lpiResult</i> parameter. When the function returns, the results of such tests are reported using the same parameter.

The IS_TEXT_UNICODE_STATISTICS and IS_TEXT_UNICODE_REVERSE_STATISTICS tests use statistical analysis. These tests are not foolproof. The statistical tests assume certain amounts of variation between low and high bytes in a string, and some ASCII strings can slip through. For example, if <i>lpv</i> indicates the ASCII string 0x41, 0x0A, 0x0D, 0x1D (A\n\r^Z), the string passes the IS_TEXT_UNICODE_STATISTICS test, although failure would be preferable.

## -see-also

<a href="/windows/desktop/Intl/unicode-and-character-set-functions">Unicode and Character Set Functions</a>



<a href="/windows/desktop/Intl/unicode-and-character-sets">Unicode and Character Sets</a>