---
UID: NF:winuser.wsprintfW
title: wsprintfW function (winuser.h)
description: Writes formatted data to the specified buffer. (Unicode)
helpviewer_keywords: ["_win32_wsprintf", "_win32_wsprintf_cpp", "menurc.wsprintf", "winui._win32_wsprintf", "winuser/wsprintf", "winuser/wsprintfW", "wsprintf", "wsprintf function [Menus and Other Resources]", "wsprintfW"]
old-location: menurc\wsprintf.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\strings\stringreference\stringfunctions\wsprintf.htm
ms.date: 12/05/2018
ms.keywords: _win32_wsprintf, _win32_wsprintf_cpp, menurc.wsprintf, winui._win32_wsprintf, winuser/wsprintf, winuser/wsprintfA, winuser/wsprintfW, wsprintf, wsprintf function [Menus and Other Resources], wsprintfA, wsprintfW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: wsprintfW (Unicode) and wsprintfA (ANSI)
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
 - wsprintfW
 - winuser/wsprintfW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - wsprintf
 - wsprintfA
 - wsprintfW
---

# wsprintfW function


## -description

Writes formatted data to the specified buffer. Any arguments are converted and copied to the output buffer according to the corresponding format specification in the format string. The function appends a terminating null character to the characters it writes, but the return value does not include the terminating null character in its character count. 
<div class="alert"><b>Note</b>  Do not use. Consider using one of the following functions instead: <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfa">StringCbPrintf</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfexa">StringCbPrintfEx</a>, <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a>, or <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfexa">StringCchPrintfEx</a>. See Security Considerations.</div><div> </div>

## -parameters

### -param unnamedParam1 [out]

Type: <b>LPTSTR</b>

The buffer that is to receive the formatted output. The maximum size of the buffer is 1,024 bytes.

### -param unnamedParam2 [in]

Type: <b>LPCTSTR</b>

The format-control specifications. In addition to ordinary ASCII characters, a format specification for each argument appears in this string. For more information about the format specification, see the Remarks section.

### -param ...

One or more optional arguments. The number and type of argument parameters depend on the corresponding format-control specifications in the <i>lpFmt</i> parameter.

## -returns

Type: <b>int</b>

If the function succeeds, the return value is the number of characters stored in the output buffer, not counting the terminating null character.

If the function fails, the return value is less than the length of the expected output. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The format-control string contains format specifications that determine the output format for the arguments following the <i>lpFmt</i> parameter. Format specifications, discussed below, always begin with a percent sign (%). If a percent sign is followed by a character that has no meaning as a format field, the character is not formatted (for example, %% produces a single percent-sign character).

The format-control string is read from left to right. When the first format specification (if any) is encountered, it causes the value of the first argument after the format-control string to be converted and copied to the output buffer according to the format specification. The second format specification causes the second argument to be converted and copied, and so on. If there are more arguments than format specifications, the extra arguments are ignored. If there are not enough arguments for all of the format specifications, the results are undefined. 

A format specification has the following form:

<b>%</b>[<b>-</b>][<b>#</b>][<b>0</b>][<i>width</i>][<i>.precision</i>]<i>type</i>

Each field is a single character or a number signifying a particular format option. The <i>type</i> characters that appear after the last optional format field determine whether the associated argument is interpreted as a character, a string, or a number. The simplest format specification contains only the percent sign and a type character (for example, %s). The optional fields control other aspects of the formatting. Following are the optional and required fields and their meanings.

				

<table class="clsStd">
<tr>
<th>Field</th>
<th>Meaning</th>
</tr>
<tr>
<td>-</td>
<td>
Pad the output with blanks or zeros to the right to fill the field width, justifying output to the left. If this field is omitted, the output is padded to the left, justifying it to the right.

</td>
</tr>
<tr>
<td>#</td>
<td>
Prefix hexadecimal values with 0x (lowercase) or 0X (uppercase).

</td>
</tr>
<tr>
<td>0</td>
<td>
Pad the output value with zeros to fill the field width. If this field is omitted, the output value is padded with blank spaces.

</td>
</tr>
<tr>
<td><i>width</i></td>
<td>
Copy the specified minimum number of characters to the output buffer. The <i>width</i> field is a nonnegative integer. The width specification never causes a value to be truncated; if the number of characters in the output value is greater than the specified width, or if the <i>width</i> field is not present, all characters of the value are printed, subject to the precision specification.

</td>
</tr>
<tr>
<td>.<i>precision</i></td>
<td>
For numbers, copy the specified minimum number of digits to the output buffer. If the number of digits in the argument is less than the specified precision, the output value is padded on the left with zeros. The value is not truncated when the number of digits exceeds the specified precision. If the specified precision is 0 or omitted entirely, or if the period (.) appears without a number following it, the precision is set to 1.

For strings, copy the specified maximum number of characters to the output buffer.

</td>
</tr>
<tr>
<td><i>type</i></td>
<td>
Output the corresponding argument as a character, a string, or a number. This field can be any of the following values.



<dl>
<dt><a id="c"></a><code>c</code></dt>
<dd>
Single character. This value is interpreted as type <b>CHAR</b> by
<b>wsprintfA</b> and type <b>WCHAR</b> by <b>wsprintfW</b>. Note
<b>wsprintf</b> is a macro defined as <b>wsprintfA</b> (Unicode not defined) or
<b>wsprintfW</b> (Unicode defined).

</dd>
<dt><a id="C"></a></a><code>C</code></dt>
<dd>
Single character. This value is interpreted as type <b>WCHAR</b> by
<b>wsprintfA</b> and type <b>CHAR</b> by <b>wsprintfW</b>. Note
<b>wsprintf</b> is a macro defined as <b>wsprintfA</b> (Unicode not defined) or
<b>wsprintfW</b> (Unicode defined).

</dd>
<dt><a id="d"></a><a id="D"></a><code>d</code></dt>
<dd>
Signed decimal integer. This value is equivalent to <code>i</code>.

</dd>
<dt><a id="hc__hC"></a><a id="hc__hc"></a><a id="HC__HC"></a><code>hc</code>, <code>hC</code></dt>
<dd>
Single character. If the character has a numeric value of zero it is ignored.
This value is always interpreted as type <b>CHAR</b>, even when the calling
application defines Unicode.

</dd>
<dt><a id="hd"></a><a id="HD"></a><code>hd</code></dt>
<dd>
Signed short integer argument.

</dd>
<dt><a id="hs__hS"></a><a id="hs__hs"></a><a id="HS__HS"></a><code>hs</code>, <code>hS</code></dt>
<dd>
String. This value is always interpreted as type <b>LPSTR</b>, even when the calling application defines Unicode.

</dd>
<dt><a id="hu"></a><a id="HU"></a><code>hu</code></dt>
<dd>
Unsigned short integer.

</dd>
<dt><a id="i"></a><a id="I"></a><code>i</code></dt>
<dd>
Signed decimal integer. This value is equivalent to <code>d</code>.

</dd>
<dt><a id="Ix__IX"></a><a id="ix__ix"></a><a id="IX__IX"></a><code>Ix</code>, <code>IX</code></dt>
<dd>
64-bit unsigned hexadecimal integer in lowercase or uppercase on 64-bit platforms, 32-bit unsigned hexadecimal integer in lowercase or uppercase on 32-bit platforms.

</dd>
<dt><a id="lc__lC"></a><a id="lc__lc"></a><a id="LC__LC"></a><code>lc</code>, <code>lC</code></dt>
<dd>
Single character. If the character has a numeric value of zero it is ignored.
This value is always interpreted as type <b>WCHAR</b>, even when the calling
application defines Unicode.

</dd>
<dt><a id="ld"></a><a id="LD"></a><code>ld</code></dt>
<dd>
Long signed integer. This value is equivalent to <code>li</code>.

</dd>
<dt><a id="li"></a><a id="LI"></a><code>li</code></dt>
<dd>
Long signed integer. This value is equivalent to <code>ld</code>.

</dd>
<dt><a id="ls__lS"></a><a id="ls__ls"></a><a id="LS__LS"></a><code>ls</code>, <code>lS</code></dt>
<dd>
String. This value is always interpreted as type <b>LPWSTR</b>, even when the calling application does not define Unicode. This value is equivalent to <code>ws</code>.

</dd>
<dt><a id="lu"></a><a id="LU"></a><code>lu</code></dt>
<dd>
Long unsigned integer.

</dd>
<dt><a id="lx__lX"></a><a id="lx__lx"></a><a id="LX__LX"></a><code>lx</code>, <code>lX</code></dt>
<dd>
Long unsigned hexadecimal integer in lowercase or uppercase.

</dd>
<dt><a id="p"></a><a id="P"></a><code>p</code></dt>
<dd>
Pointer. The address is printed using hexadecimal.

</dd>
<dt><a id="s"></a><a id="S"></a><code>s</code></dt>
<dd>
String. This value is interpreted as type <b>LPSTR</b> by <b>wsprintfA</b> and
type <b>LPWSTR</b> by <b>wsprintfW</b>. Note <b>wsprintf</b> is a macro defined
as <b>wsprintfA</b> (Unicode not defined) or <b>wsprintfW</b> (Unicode
defined).

</dd>
<dt><a id="S"></a><a id="s"></a><code>S</code></dt>
<dd>
String. This value is interpreted as type <b>LPWSTR</b> by <b>wsprintfA</b> and
type <b>LPSTR</b> by <b>wsprintfW</b>. Note <b>wsprintf</b> is a macro defined
as <b>wsprintfA</b> (Unicode not defined) or <b>wsprintfW</b> (Unicode
defined).

</dd>
<dt><a id="u"></a><a id="U"></a><code>u</code></dt>
<dd>
Unsigned integer argument.

</dd>
<dt><a id="x__X"></a><a id="x__x"></a><a id="X__X"></a><code>x</code>, <code>X</code></dt>
<dd>
Unsigned hexadecimal integer in lowercase or uppercase.

</dd>
</dl>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  It is important to note that <b>wsprintf</b> uses the C calling convention (<b>_cdecl</b>), rather than the standard call (<b>_stdcall</b>) calling convention. As a result, it is the responsibility of the calling process to pop arguments off the stack, and arguments are pushed on the stack from right to left. In C-language modules, the C compiler performs this task.</div>
<div> </div>
To use buffers larger than 1024 bytes, use <b>_snwprintf</b>. For more information, see the documentation for the C run-time library. 





> [!NOTE]
> The winuser.h header defines wsprintf as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfa">StringCbPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbprintfexa">StringCbPrintfEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfa">StringCbVPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfexa">StringCbVPrintfEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfa">StringCchPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchprintfexa">StringCchPrintfEx</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfa">StringCchVPrintf</a>



<a href="/windows/desktop/api/strsafe/nf-strsafe-stringcchvprintfexa">StringCchVPrintfEx</a>



<a href="/windows/desktop/menurc/strings">Strings</a>



<a href="/windows/desktop/api/winuser/nf-winuser-wvsprintfa">wvsprintf</a>

