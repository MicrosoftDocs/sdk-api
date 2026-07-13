---
UID: NF:strsafe.StringCbVPrintf_lW
title: StringCbVPrintf_lW function (strsafe.h)
description: Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer. (StringCbVPrintf_lW)
helpviewer_keywords: ["StringCbVPrintf_l", "StringCbVPrintf_l function [Menus and Other Resources]", "StringCbVPrintf_lW", "menurc.stringcbvprintf_l", "strsafe/StringCbVPrintf_l", "strsafe/StringCbVPrintf_lW"]
old-location: menurc\stringcbvprintf_l.htm
tech.root: menurc
ms.assetid: e3e39151-03f7-4d85-91a0-d353122e6b4b
ms.date: 12/05/2018
ms.keywords: StringCbVPrintf_l, StringCbVPrintf_l function [Menus and Other Resources], StringCbVPrintf_lA, StringCbVPrintf_lW, menurc.stringcbvprintf_l, strsafe/StringCbVPrintf_l, strsafe/StringCbVPrintf_lA, strsafe/StringCbVPrintf_lW
req.header: strsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StringCbVPrintf_lW (Unicode) and StringCbVPrintf_lA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StringCbVPrintf_lW
 - strsafe/StringCbVPrintf_lW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - StrSafe.h
api_name:
 - StringCbVPrintf_l
 - StringCbVPrintf_lA
 - StringCbVPrintf_lW
---

# StringCbVPrintf_lW function


## -description

Writes formatted data to the specified string using a pointer to a list of arguments. The size of the destination buffer is provided to the function to ensure that it does not write past the end of this buffer.

<b>StringCbVPrintf_l</b> is similar to <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintfa">StringCbVPrintf</a> but includes a parameter for locale information.

## -parameters

### -param pszDest [out]

The destination buffer, which receives the formatted, null-terminated string created from <i>pszFormat</i> and <i>argList</i>.

### -param cbDest [in]

The size of the destination buffer, in bytes. This value must be sufficiently large to accommodate the final formatted string plus the terminating null character. The maximum number of bytes allowed is <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.

### -param pszFormat [in]

The format string. This string must be null-terminated. For more information, see <a href="/cpp/c-runtime-library/format-specification-syntax-printf-and-wprintf-functions">Format Specification Syntax</a>.

### -param locale [in]

The locale object. For more information, see <b>_create_locale</b>.

### -param argList [in]

The arguments to be inserted into the <i>pszFormat</i> string.

## -returns

This function can return one of the following values. It is strongly recommended that you use the <a href="/windows/desktop/api/winerror/nf-winerror-succeeded">SUCCEEDED</a> and <a href="/windows/desktop/api/winerror/nf-winerror-failed">FAILED</a> macros to test the return value of this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
There was sufficient space for the result to be copied to <i>pszDest</i> without truncation, and the buffer is null-terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The value in <i>cbDest</i> is either 0 or larger than <code>STRSAFE_MAX_CCH * sizeof(TCHAR)</code>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STRSAFE_E_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed due to insufficient buffer space. The destination buffer contains a truncated, null-terminated version of the intended result. In situations where truncation is acceptable, this may not necessarily be seen as a failure condition.

</td>
</tr>
</table>

## -remarks

For more information on va_lists, see the conventions defined in Stdarg.h.

Behavior is undefined if the strings pointed to by <i>pszDest</i>, <i>pszFormat</i>, or any argument strings overlap.

Neither <i>pszFormat</i> nor <i>pszDest</i> should be <b>NULL</b>. See <a href="/windows/desktop/api/strsafe/nf-strsafe-stringcbvprintf_lexa">StringCbVPrintf_lEx</a> if you require the handling of null string pointer values.

In order to use this function, you must define the following macro in your header file, before including StrSafe.h.

<code>#define STRSAFE_LOCALE_FUNCTIONS</code>




> [!NOTE]
> The strsafe.h header defines StringCbVPrintf_l as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
