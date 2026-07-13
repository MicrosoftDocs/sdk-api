---
UID: NF:shlwapi.UrlCombineW
title: UrlCombineW function (shlwapi.h)
description: When provided with a relative URL and its base, returns a URL in canonical form. (Unicode)
helpviewer_keywords: ["URL_DONT_SIMPLIFY", "URL_ESCAPE_AS_UTF8", "URL_ESCAPE_PERCENT", "URL_ESCAPE_SPACES_ONLY", "URL_ESCAPE_UNSAFE", "URL_NO_META", "URL_PLUGGABLE_PROTOCOL", "URL_UNESCAPE", "UrlCombine", "UrlCombine function [Windows Shell]", "UrlCombineW", "_win32_UrlCombine", "shell.UrlCombine", "shlwapi/UrlCombine", "shlwapi/UrlCombineW"]
old-location: shell\UrlCombine.htm
tech.root: shell
ms.assetid: f574d365-1ab9-4de4-84fe-17820c327ccf
ms.date: 12/05/2018
ms.keywords: URL_DONT_SIMPLIFY, URL_ESCAPE_AS_UTF8, URL_ESCAPE_PERCENT, URL_ESCAPE_SPACES_ONLY, URL_ESCAPE_UNSAFE, URL_NO_META, URL_PLUGGABLE_PROTOCOL, URL_UNESCAPE, UrlCombine, UrlCombine function [Windows Shell], UrlCombineA, UrlCombineW, _win32_UrlCombine, shell.UrlCombine, shlwapi/UrlCombine, shlwapi/UrlCombineA, shlwapi/UrlCombineW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlCombineW (Unicode) and UrlCombineA (ANSI)
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
 - UrlCombineW
 - shlwapi/UrlCombineW
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
 - UrlCombine
 - UrlCombineA
 - UrlCombineW
---

# UrlCombineW function


## -description

When provided with a relative URL and its base, returns a URL in canonical form.

## -parameters

### -param pszBase [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the base URL.

### -param pszRelative [in]

Type: <b>PCTSTR</b>

A pointer to a null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the relative URL.

### -param pszCombined [out, optional]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives a null-terminated string that contains the combined URL.

### -param pcchCombined [in, out]

Type: <b>DWORD*</b>

A pointer to a value that, on entry, is set to the number of characters in the <i>pszCombined</i> buffer. When the function returns successfully, the value depends on whether the function is successful or returns E_POINTER. For other return values, the value of this parameter is meaningless.

### -param dwFlags

Type: <b>DWORD</b>

Flags that specify how the URL is converted to canonical form. The following flags can be combined.



#### URL_DONT_SIMPLIFY (0x08000000)

Treat '/./' and '/../' in a URL string as literal characters, not as shorthand for navigation. See Remarks for further discussion.



#### URL_ESCAPE_PERCENT (0x00001000)

Convert any occurrence of '%' to its escape sequence.



#### URL_ESCAPE_SPACES_ONLY (0x04000000)

Replace only spaces with escape sequences. This flag takes precedence over <b>URL_ESCAPE_UNSAFE</b>, but does not apply to opaque URLs.



#### URL_ESCAPE_UNSAFE (0x20000000)

Replace unsafe characters with their escape sequences. Unsafe characters are those characters that may be altered during transport across the Internet, and include the (&lt;, &gt;, ", #, {, }, |, \, ^, ~, [, ], and ') characters. This flag applies to all URLs, including opaque URLs.



#### URL_NO_META

Defined to be the same as <b>URL_DONT_SIMPLIFY</b>.



#### URL_PLUGGABLE_PROTOCOL (0x40000000)

Combine URLs with client-defined pluggable protocols, according to the W3C specification. This flag does not apply to standard protocols such as ftp, http, gopher, and so on. If this flag is set, <b>UrlCombine</b> does not simplify URLs, so there is no need to also set <b>URL_DONT_SIMPLIFY</b>.



#### URL_UNESCAPE (0x10000000)

Un-escape any escape sequences that the URLs contain, with two exceptions. The escape sequences for '?' and '#' are not un-escaped. If one of the URL_ESCAPE_XXX flags is also set, the two URLs are first un-escaped, then combined, then escaped.



#### URL_ESCAPE_AS_UTF8 (0x00040000)

<b>Windows 7 and later</b>. Percent-encode all non-ASCII characters as their UTF-8 equivalents.


##### - dwFlags.URL_DONT_SIMPLIFY (0x08000000)

Treat '/./' and '/../' in a URL string as literal characters, not as shorthand for navigation. See Remarks for further discussion.


##### - dwFlags.URL_ESCAPE_AS_UTF8 (0x00040000)

<b>Windows 7 and later</b>. Percent-encode all non-ASCII characters as their UTF-8 equivalents.


##### - dwFlags.URL_ESCAPE_PERCENT (0x00001000)

Convert any occurrence of '%' to its escape sequence.


##### - dwFlags.URL_ESCAPE_SPACES_ONLY (0x04000000)

Replace only spaces with escape sequences. This flag takes precedence over <b>URL_ESCAPE_UNSAFE</b>, but does not apply to opaque URLs.


##### - dwFlags.URL_ESCAPE_UNSAFE (0x20000000)

Replace unsafe characters with their escape sequences. Unsafe characters are those characters that may be altered during transport across the Internet, and include the (&lt;, &gt;, ", #, {, }, |, \, ^, ~, [, ], and ') characters. This flag applies to all URLs, including opaque URLs.


##### - dwFlags.URL_NO_META

Defined to be the same as <b>URL_DONT_SIMPLIFY</b>.


##### - dwFlags.URL_PLUGGABLE_PROTOCOL (0x40000000)

Combine URLs with client-defined pluggable protocols, according to the W3C specification. This flag does not apply to standard protocols such as ftp, http, gopher, and so on. If this flag is set, <b>UrlCombine</b> does not simplify URLs, so there is no need to also set <b>URL_DONT_SIMPLIFY</b>.


##### - dwFlags.URL_UNESCAPE (0x10000000)

Un-escape any escape sequences that the URLs contain, with two exceptions. The escape sequences for '?' and '#' are not un-escaped. If one of the URL_ESCAPE_XXX flags is also set, the two URLs are first un-escaped, then combined, then escaped.

## -returns

Type: <b>HRESULT</b>

Returns standard COM error codes, including the following.

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
<i>pszCombined</i> points to a string that contains the combined URLs. The value of <i>pcchCombined</i> is set to the number of characters in the string, not counting the terminating <b>NULL</b> character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The buffer was too small. The value of <i>pcchCombined</i> is set to the minimum number of characters that the buffer must be able to contain, including the terminating <b>NULL</b> character.

</td>
</tr>
</table>

## -remarks

Items between slashes are treated as hierarchical identifiers; the last item specifies the document itself. You must enter a slash (/) after the document name to append more items; otherwise, <b>UrlCombine</b> exchanges one document for another. For example: 		

				


```

hRetVal = UrlCombine(TEXT("http://xyz/test/abc"), 
                     TEXT("bar"), 
                     lpszCombined, 
                     &dwLength, 0);
```


The preceding code returns the URL http://xyz/test/bar. If you want the combined URL to be http://xyz/test/abc/bar, use the following call to <b>UrlCombine</b>.

				


```

hRetVal = UrlCombine(TEXT("http://xyz/test/abc/"), 
                     TEXT("bar"), 
                     lpszCombined, 
                     &dwLength, 0);
```


If a URL string contains '/../' or '/./', <b>UrlCombine</b> usually treats the characters as if they indicated navigation in the URL hierarchy. The function simplifies the URLs before combining them. For instance, "/hello/cruel/../world" is simplified to "/hello/world". If the <b>URL_DONT_SIMPLIFY</b> flag is set in <i>dwFlags</i>, the function does not simplify URLs. In this case, "/hello/cruel/../world" is left as it is.





> [!NOTE]
> The shlwapi.h header defines UrlCombine as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/WinInet/handling-uniform-resource-locators">Handling Uniform Resource Locators</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-urlcanonicalizea">UrlCanonicalize</a>
