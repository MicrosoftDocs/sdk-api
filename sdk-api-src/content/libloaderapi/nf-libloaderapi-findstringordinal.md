---
UID: NF:libloaderapi.FindStringOrdinal
title: FindStringOrdinal function (libloaderapi.h)
description: Locates a Unicode string (wide characters) in another Unicode string for a non-linguistic comparison.
helpviewer_keywords: ["FIND_ENDSWITH","FIND_FROMEND","FIND_FROMSTART","FIND_STARTSWITH","FindStringOrdinal","FindStringOrdinal function [Internationalization for Windows Applications]","intl.findstringordinal","libloaderapi/FindStringOrdinal"]
old-location: intl\findstringordinal.htm
tech.root: Intl
ms.assetid: 6aca64f5-640a-4be6-9606-260314e9c7dc
ms.date: 12/05/2018
ms.keywords: FIND_ENDSWITH, FIND_FROMEND, FIND_FROMSTART, FIND_STARTSWITH, FindStringOrdinal, FindStringOrdinal function [Internationalization for Windows Applications], intl.findstringordinal, libloaderapi/FindStringOrdinal
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindStringOrdinal
 - libloaderapi/FindStringOrdinal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - FindStringOrdinal
---

# FindStringOrdinal function


## -description

Locates a Unicode string (wide characters) in another Unicode string for a non-linguistic comparison.

## -parameters

### -param dwFindStringOrdinalFlags [in]

Flags specifying details of the find operation. These flags are mutually exclusive, with FIND_FROMSTART being the default. The application can specify just one of the find flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FIND_FROMSTART"></a><a id="find_fromstart"></a><dl>
<dt><b>FIND_FROMSTART</b></dt>
</dl>
</td>
<td width="60%">
Search the string, starting with the first character of the string.

</td>
</tr>
<tr>
<td width="40%"><a id="FIND_FROMEND"></a><a id="find_fromend"></a><dl>
<dt><b>FIND_FROMEND</b></dt>
</dl>
</td>
<td width="60%">
Search the string in the reverse direction, starting with the last character of the string.

</td>
</tr>
<tr>
<td width="40%"><a id="FIND_STARTSWITH"></a><a id="find_startswith"></a><dl>
<dt><b>FIND_STARTSWITH</b></dt>
</dl>
</td>
<td width="60%">
Test to find out if the value specified by <i>lpStringValue</i> is the first value in the source string indicated by <i>lpStringSource</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="FIND_ENDSWITH"></a><a id="find_endswith"></a><dl>
<dt><b>FIND_ENDSWITH</b></dt>
</dl>
</td>
<td width="60%">
Test to find out if the value specified by <i>lpStringValue</i> is the last value in the source string indicated by <i>lpStringSource</i>.

</td>
</tr>
</table>

### -param lpStringSource [in]

Pointer to the source string, in which the function searches for the string specified by <i>lpStringValue</i>.

### -param cchSource [in]

Size, in characters excluding the terminating null character, of the string indicated by <i>lpStringSource</i>. The application must normally specify a positive number, or 0. The application can specify -1 if the source string is null-terminated and the function should calculate the size automatically.

### -param lpStringValue [in]

Pointer to the search string for which the function searches in the source string.

### -param cchValue [in]

Size, in characters excluding the terminating null character, of the string indicated by <i>lpStringValue</i>. The application must normally specify a positive number, or 0. The application can specify -1 if the string is null-terminated and the function should calculate the size automatically.

### -param bIgnoreCase [in]

<b>TRUE</b> if the function is to perform a case-insensitive comparison, and <b>FALSE</b> otherwise. The comparison is not a linguistic operation and is not appropriate for all locales and languages. Its behavior is similar to that for English.

## -returns

Returns a 0-based index into the source string indicated by <i>lpStringSource</i> if successful. If the function succeeds, the found string is the same size as the value of <i>lpStringValue</i>. A return value of 0 indicates that the function found a match at the beginning of the source string.

The function returns -1 if it does not succeed or if it does not find the search string. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which can return one of the following error codes:

<ul>
<li>ERROR_INVALID_FLAGS. The values supplied for flags were not valid.</li>
<li>ERROR_INVALID_PARAMETER. Any of the parameter values was invalid.</li>
<li>ERROR_SUCCESS. The action completed successfully but yielded no results.</li>
</ul>

## -remarks

Since <b>FindStringOrdinal</b> provides a binary comparison, it does not return linguistically appropriate results. The ordinal comparison might be mistaken for English sorting behavior. However, it does not find matches when characters vary by linguistically insignificant amounts. See <a href="/windows/desktop/Intl/sorting">Sorting</a> for information about choosing an appropriate sorting function.

In contrast to NLS functions that return 0 for failure, this function returns -1 if it fails. On success, it returns a 0-based index. Use of this index helps the function avoid off-by-one errors and one-character buffer overruns.

This function is one of the few NLS functions that calls <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> even when it succeeds. It makes this call to clear the last error in a thread when it fails to match the search string. This clears the value returned by <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

<b>Starting with Windows 8: </b><b>FindStringOrdinal</b>  is declared in Libloaderapi.h. Before Windows 8, it was declared in Winnls.h.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-findnlsstring">FindNLSString</a>



<a href="/windows/desktop/api/winnls/nf-winnls-findnlsstringex">FindNLSStringEx</a>



<a href="/windows/desktop/Intl/handling-sorting-in-your-applications">Handling Sorting in Your Applications</a>



<a href="/windows/desktop/Intl/national-language-support">National Language Support</a>



<a href="/windows/desktop/Intl/national-language-support-functions">National Language Support Functions</a>