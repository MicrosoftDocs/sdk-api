---
UID: NF:winnls.IsDBCSLeadByte
title: IsDBCSLeadByte function (winnls.h)
description: Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP_ACP). A lead byte is the first byte of a two-byte character in a double-byte character set (DBCS) for the code page.
helpviewer_keywords: ["IsDBCSLeadByte","IsDBCSLeadByte function [Internationalization for Windows Applications]","_win32_IsDBCSLeadByte","intl.isdbcsleadbyte","winnls/IsDBCSLeadByte"]
old-location: intl\isdbcsleadbyte.htm
tech.root: Intl
ms.assetid: 13767af5-9313-4c11-8386-fe41c7720d49
ms.date: 12/05/2018
ms.keywords: IsDBCSLeadByte, IsDBCSLeadByte function [Internationalization for Windows Applications], _win32_IsDBCSLeadByte, intl.isdbcsleadbyte, winnls/IsDBCSLeadByte
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsDBCSLeadByte
 - winnls/IsDBCSLeadByte
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-localization-l1-2-4.dll
 - api-ms-win-core-localization-l1-2-3.dll
 - kernel32.dll
 - API-MS-Win-Core-Localization-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Localization-l1-2-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Localization-L1-2-2.dll
api_name:
 - IsDBCSLeadByte
---

# IsDBCSLeadByte function


## -description

Determines if a specified character is a lead byte for the system default Windows ANSI code page 
    (<b>CP_ACP</b>). A lead byte is the first byte of a two-byte character in a 
    <a href="/windows/desktop/Intl/double-byte-character-sets">double-byte character set</a> (DBCS) for the code 
    page.
<div class="alert"><b>Note</b>  To use a different code page, your application should use the 
    <a href="/windows/desktop/api/winnls/nf-winnls-isdbcsleadbyteex">IsDBCSLeadByteEx</a> function.</div><div> </div>

## -parameters

### -param TestChar [in]

The character to test.

## -returns

Returns a nonzero value if the test character is potentially a lead byte. The function returns 0 if the test 
       character is not a lead byte or if it is a single-byte character. To get extended error information, the 
       application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<div class="alert"><b>Note</b>  This function does not validate the presence or validity of a trail byte. Therefore, 
     <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> might not recognize a 
     sequence that the application using <b>IsDBCSLeadByte</b> 
     reports as a lead byte. The application can easily become unsynchronized with the results of 
     <b>MultiByteToWideChar</b>, potentially leading to 
     unexpected errors or buffer size mismatches.</div>
<div> </div>
In general, instead of attempting low-level manipulation of code page data, applications should use 
    <a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> to convert the 
    data to UTF-16 and work with it in that encoding.

Lead byte values are specific to each distinct DBCS. Some byte values can appear in a single code page as both 
    the lead and trail byte of a DBCS character.

To make sense of a DBCS string, an application normally starts at the beginning of a string and scans forward, 
    keeping track when it encounters a lead byte, and treating the next byte as the trailing part of the same 
    character. If the application must back up, it should use 
    <a href="/windows/desktop/menurc/v">CharPrev</a> instead of attempting to develop its own 
    algorithm.

## -see-also

<a href="/windows/desktop/api/winnls/nf-winnls-isdbcsleadbyteex">IsDBCSLeadByteEx</a>



<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a>



<a href="/windows/desktop/Intl/unicode-and-character-set-functions">Unicode and Character Set Functions</a>



<a href="/windows/desktop/Intl/unicode-and-character-sets">Unicode and Character Sets</a>