---
UID: NF:shlwapi.UrlCanonicalizeW
title: UrlCanonicalizeW function (shlwapi.h)
description: Converts a URL string into canonical form. (Unicode)
helpviewer_keywords: ["URL_DONT_SIMPLIFY", "URL_ESCAPE_AS_UTF8", "URL_ESCAPE_PERCENT", "URL_ESCAPE_SPACES_ONLY", "URL_ESCAPE_UNSAFE", "URL_NO_META", "URL_PLUGGABLE_PROTOCOL", "URL_UNESCAPE", "UrlCanonicalize", "UrlCanonicalize function [Windows Shell]", "UrlCanonicalizeW", "_win32_UrlCanonicalize", "shell.UrlCanonicalize", "shlwapi/UrlCanonicalize", "shlwapi/UrlCanonicalizeW"]
old-location: shell\UrlCanonicalize.htm
tech.root: shell
ms.assetid: 70802745-0611-4d37-800e-b50d5ea23426
ms.date: 12/05/2018
ms.keywords: URL_DONT_SIMPLIFY, URL_ESCAPE_AS_UTF8, URL_ESCAPE_PERCENT, URL_ESCAPE_SPACES_ONLY, URL_ESCAPE_UNSAFE, URL_NO_META, URL_PLUGGABLE_PROTOCOL, URL_UNESCAPE, UrlCanonicalize, UrlCanonicalize function [Windows Shell], UrlCanonicalizeA, UrlCanonicalizeW, _win32_UrlCanonicalize, shell.UrlCanonicalize, shlwapi/UrlCanonicalize, shlwapi/UrlCanonicalizeA, shlwapi/UrlCanonicalizeW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlCanonicalizeW (Unicode) and UrlCanonicalizeA (ANSI)
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
 - UrlCanonicalizeW
 - shlwapi/UrlCanonicalizeW
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
 - UrlCanonicalize
 - UrlCanonicalizeA
 - UrlCanonicalizeW
---

# UrlCanonicalizeW function


## -description

Converts a URL string into canonical form.

## -parameters

### -param pszUrl [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains a URL string. If the string does not refer to a file, it must include a valid scheme such as "http://".

### -param pszCanonicalized [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the converted URL as a null-terminated string.

### -param pcchCanonicalized [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, on entry, is set to the number of characters in the <i>pszCanonicalized</i> buffer.

### -param dwFlags

Type: <b>DWORD</b>

The flags that specify how the URL is converted to canonical form. The following flags can be combined.



#### URL_UNESCAPE (0x10000000)

Un-escape any escape sequences that the URLs contain, with two exceptions. The escape sequences for "?" and "#" are not un-escaped. If one of the URL_ESCAPE_XXX flags is also set, the two URLs are first un-escaped, then combined, then escaped.



#### URL_ESCAPE_UNSAFE (0x20000000)

Replace unsafe characters with their escape sequences. Unsafe characters are those characters that may be altered during transport across the Internet, and include the (&lt;, &gt;, ", #, {, }, |, \, ^, [, ], and ') characters. This flag applies to all URLs, including opaque URLs.



#### URL_PLUGGABLE_PROTOCOL (0x40000000)

Combine URLs with client-defined pluggable protocols, according to the W3C specification. This flag does not apply to standard protocols such as ftp, http, gopher, and so on. If this flag is set, <a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlcombinea">UrlCombine</a> does not simplify URLs, so there is no need to also set <b>URL_DONT_SIMPLIFY</b>.



#### URL_ESCAPE_SPACES_ONLY (0x04000000)

Replace only spaces with escape sequences. This flag takes precedence over <b>URL_ESCAPE_UNSAFE</b>, but does not apply to opaque URLs.



#### URL_DONT_SIMPLIFY (0x08000000)

Treat "/./" and "/../" in a URL string as literal characters, not as shorthand for navigation. See Remarks for further discussion.



#### URL_NO_META (0x08000000)

Defined to be the same as <b>URL_DONT_SIMPLIFY</b>.



#### URL_ESCAPE_PERCENT (0x00001000)

Convert any occurrence of "%" to its escape sequence.



#### URL_ESCAPE_AS_UTF8 (0x00040000)

<b>Windows 7 and later</b>. Percent-encode all non-ASCII characters as their UTF-8 equivalents.


##### - dwFlags.URL_DONT_SIMPLIFY (0x08000000)

Treat "/./" and "/../" in a URL string as literal characters, not as shorthand for navigation. See Remarks for further discussion.


##### - dwFlags.URL_ESCAPE_AS_UTF8 (0x00040000)

<b>Windows 7 and later</b>. Percent-encode all non-ASCII characters as their UTF-8 equivalents.


##### - dwFlags.URL_ESCAPE_PERCENT (0x00001000)

Convert any occurrence of "%" to its escape sequence.


##### - dwFlags.URL_ESCAPE_SPACES_ONLY (0x04000000)

Replace only spaces with escape sequences. This flag takes precedence over <b>URL_ESCAPE_UNSAFE</b>, but does not apply to opaque URLs.


##### - dwFlags.URL_ESCAPE_UNSAFE (0x20000000)

Replace unsafe characters with their escape sequences. Unsafe characters are those characters that may be altered during transport across the Internet, and include the (&lt;, &gt;, ", #, {, }, |, \, ^, [, ], and ') characters. This flag applies to all URLs, including opaque URLs.


##### - dwFlags.URL_NO_META (0x08000000)

Defined to be the same as <b>URL_DONT_SIMPLIFY</b>.


##### - dwFlags.URL_PLUGGABLE_PROTOCOL (0x40000000)

Combine URLs with client-defined pluggable protocols, according to the W3C specification. This flag does not apply to standard protocols such as ftp, http, gopher, and so on. If this flag is set, <a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlcombinea">UrlCombine</a> does not simplify URLs, so there is no need to also set <b>URL_DONT_SIMPLIFY</b>.


##### - dwFlags.URL_UNESCAPE (0x10000000)

Un-escape any escape sequences that the URLs contain, with two exceptions. The escape sequences for "?" and "#" are not un-escaped. If one of the URL_ESCAPE_XXX flags is also set, the two URLs are first un-escaped, then combined, then escaped.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function performs such tasks as replacing unsafe characters with their escape sequences and collapsing sequences like "..\...".

If a URL string contains "/../" or "/./", <b>UrlCanonicalize</b> treats the characters as indicating navigation in the URL hierarchy. The function simplifies the URLs before combining them. For instance "/hello/cruel/../world" is simplified to "/hello/world". Exceptions to this default behavior occur in these cases:
                
                

<ul>
<li>If the <b>URL_DONT_SIMPLIFY</b> flag is set in <i>dwFlags</i>, the function does not simplify URLs. In this case, "/hello/cruel/../world" is left as it is.</li>
<li>If "/../" or "/./" is the first segment in the path (for example, "http://domain/../path1/path2/file.htm"), <b>UrlCanonicalize</b> outputs the path exactly as it was input.</li>
</ul>




> [!NOTE]
> The shlwapi.h header defines UrlCanonicalize as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/handling-uniform-resource-locators">Handling Uniform Resource Locators</a>
