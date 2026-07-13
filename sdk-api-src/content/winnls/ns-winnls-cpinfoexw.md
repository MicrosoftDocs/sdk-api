---
UID: NS:winnls._cpinfoexW
title: CPINFOEXW (winnls.h)
description: Contains information about a code page. This structure is used by the GetCPInfoEx function. (Unicode)
helpviewer_keywords: ["*LPCPINFOEXW","CPINFOEX","CPINFOEX structure [Internationalization for Windows Applications]","CPINFOEXW","LPCPINFOEX","LPCPINFOEX structure pointer [Internationalization for Windows Applications]","_win32_CPINFOEX_str","intl.cpinfoex","winnls/CPINFOEX","winnls/LPCPINFOEX"]
old-location: intl\cpinfoex.htm
tech.root: Intl
ms.assetid: 9639bb11-477e-45ee-b9fb-d5d099925e00
ms.date: 12/05/2018
ms.keywords: '*LPCPINFOEXW, CPINFOEX, CPINFOEX structure [Internationalization for Windows Applications], CPINFOEXW, LPCPINFOEX, LPCPINFOEX structure pointer [Internationalization for Windows Applications], _win32_CPINFOEX_str, intl.cpinfoex, winnls/CPINFOEX, winnls/LPCPINFOEX'
req.header: winnls.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CPINFOEXW, *LPCPINFOEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _cpinfoexW
 - winnls/_cpinfoexW
 - LPCPINFOEXW
 - winnls/LPCPINFOEXW
 - CPINFOEXW
 - winnls/CPINFOEXW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnls.h
api_name:
 - CPINFOEX
---

# CPINFOEXW structure


## -description

Contains information about a code page. This structure is used by the <a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a> function.

## -struct-fields

### -field MaxCharSize

Maximum length, in bytes, of a character in the code page. The length can be 1 for a <a href="/windows/desktop/Intl/single-byte-character-sets">single-byte character set</a> (SBCS), 2 for a <a href="/windows/desktop/Intl/double-byte-character-sets">double-byte character set</a> (DBCS), or a value larger than 2 for other character set types. The function cannot use the size to distinguish an SBCS or a DBCS from other character sets because of other factors, for example, the use of ISCII or ISO-2022-xx code pages.

### -field DefaultChar

Default character used when translating character strings to the specific code page. This character is used by the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> function if an explicit default character is not specified. The default is usually the "?" character for the code page.

### -field LeadByte

A fixed-length array of lead byte ranges, for which the number of lead byte ranges is variable. If the code page has no lead bytes, every element of the array is set to <b>NULL</b>. If the code page has lead bytes, the array specifies a starting value and an ending value for each range. Ranges are inclusive, and the maximum number of ranges for any code page is five. The array uses two bytes to describe each range, with two null bytes as a terminator after the last range.

<div class="alert"><b>Note</b>   Some code pages use lead bytes and a combination of other encoding mechanisms. This member is usually only populated for a subset of the code pages that use lead bytes in some form. For more information, see the Remarks section.</div>
<div> </div>

### -field UnicodeDefaultChar

Unicode default character used in translations from the specific code page. The default is usually the "?" character or the katakana middle dot character. The Unicode default character is used by the <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> function.

### -field CodePage

Code page value. This value reflects the code page passed to the <a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a> function. See <a href="/windows/desktop/Intl/code-page-identifiers">Code Page Identifiers</a> for a list of ANSI and other code pages.

### -field CodePageName

Full name of the code page. Note that this name is localized and is not guaranteed for uniqueness or consistency between operating system versions or computers.

## -remarks

Lead bytes are unique to DBCS code pages that allow for more than 256 characters. A lead byte is the first byte of a 2-byte character in a DBCS. On each DBCS code page, the lead bytes occupy a specific range of byte values. This range is different for different code pages.

The lead byte information is not very helpful for most code pages, and is not even provided for many multi-byte encodings, for example, UTF-8 and GB18030. Your applications are discouraged from using this information to predict what the       <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> or <a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a> function will do. The function might end up using a default character or performing other default behavior if the bytes following the lead byte are not as expected.





> [!NOTE]
> The winnls.h header defines CPINFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-getcpinfoexa">GetCPInfoEx</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<a href="/windows/desktop/Intl/national-language-support-structures">National Language Support Structures</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte">WideCharToMultiByte</a>
