---
UID: NF:shlwapi.UrlApplySchemeW
title: UrlApplySchemeW function (shlwapi.h)
description: Determines a scheme for a specified URL string, and returns a string with an appropriate prefix. (Unicode)
helpviewer_keywords: ["URL_APPLY_DEFAULT", "URL_APPLY_FORCEAPPLY", "URL_APPLY_GUESSFILE", "URL_APPLY_GUESSSCHEME", "UrlApplyScheme", "UrlApplyScheme function [Windows Shell]", "UrlApplySchemeW", "_win32_UrlApplyScheme", "shell.UrlApplyScheme", "shlwapi/UrlApplyScheme", "shlwapi/UrlApplySchemeW"]
old-location: shell\UrlApplyScheme.htm
tech.root: shell
ms.assetid: af60643e-b1a4-4013-b116-dd9fad4e90bf
ms.date: 12/05/2018
ms.keywords: URL_APPLY_DEFAULT, URL_APPLY_FORCEAPPLY, URL_APPLY_GUESSFILE, URL_APPLY_GUESSSCHEME, UrlApplyScheme, UrlApplyScheme function [Windows Shell], UrlApplySchemeA, UrlApplySchemeW, _win32_UrlApplyScheme, shell.UrlApplyScheme, shlwapi/UrlApplyScheme, shlwapi/UrlApplySchemeA, shlwapi/UrlApplySchemeW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlApplySchemeW (Unicode) and UrlApplySchemeA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UrlApplySchemeW
 - shlwapi/UrlApplySchemeW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - UrlApplyScheme
 - UrlApplySchemeA
 - UrlApplySchemeW
---

# UrlApplySchemeW function


## -description

Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.

## -parameters

### -param pszIn [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains a URL.

### -param pszOut [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives a null-terminated string set to the URL specified by <i>pszIn</i> and converted to the standard <i>scheme</i>://<i>URL_string</i> format.

### -param pcchOut [in, out]

Type: <b>DWORD*</b>

The address of a value set to the number of characters in the <i>pszOut</i> buffer. When the function returns, the value depends on whether the function is successful or returns E_POINTER. For other return values, the value of this parameter is meaningless.

### -param dwFlags

Type: <b>DWORD</b>

The flags that specify how to determine the scheme. The following flags can be combined.



#### URL_APPLY_DEFAULT

Apply the default scheme if <b>UrlApplyScheme</b> can't determine one. The default prefix is stored in the registry but is typically "http".



#### URL_APPLY_GUESSSCHEME

Attempt to determine the scheme by examining <i>pszIn</i>.



#### URL_APPLY_GUESSFILE

Attempt to determine a file URL from <i>pszIn</i>.



#### URL_APPLY_FORCEAPPLY

Force <b>UrlApplyScheme</b> to determine a scheme for pszIn.


##### - dwFlags.URL_APPLY_DEFAULT

Apply the default scheme if <b>UrlApplyScheme</b> can't determine one. The default prefix is stored in the registry but is typically "http".


##### - dwFlags.URL_APPLY_FORCEAPPLY

Force <b>UrlApplyScheme</b> to determine a scheme for pszIn.


##### - dwFlags.URL_APPLY_GUESSFILE

Attempt to determine a file URL from <i>pszIn</i>.


##### - dwFlags.URL_APPLY_GUESSSCHEME

Attempt to determine the scheme by examining <i>pszIn</i>.

## -returns

Type: <b>HRESULT</b>

Returns a standard COM return value, including the following.

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
A scheme was determined. pszOut points to a string containing the URL with the scheme's prefix. The value of <i>pcchOut</i> is set to the number of characters in the string, not counting the terminating <b>NULL</b> character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There were no errors, but no prefix was prepended.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The buffer was too small. The value of <i>pcchOut</i> is set to the minimum number of characters that the buffer must be able to contain, including the terminating <b>NULL</b> character.

</td>
</tr>
</table>

## -remarks

If the URL has a valid scheme, the string will not be modified. However, almost any combination of two or more characters followed by a colon will be parsed as a scheme. Valid characters include some common punctuation marks, such as ".". If your input string fits this description, <b>UrlApplyScheme</b> may treat it as valid and not apply a scheme. To force the function to apply a scheme to a URL, set the <b>URL_APPLY_FORCEAPPLY</b> and <b>URL_APPLY_DEFAULT</b> flags in <i>dwFlags</i>. This combination of flags forces the function to apply a scheme to the URL. Typically, the function will not be able to determine a valid scheme. The second flag guarantees that, if no valid scheme can be determined, the function will apply the default scheme to the URL.




> [!NOTE]
> The shlwapi.h header defines UrlApplyScheme as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

