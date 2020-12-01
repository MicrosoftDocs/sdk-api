---
UID: NF:shlwapi.UrlFixupW
title: UrlFixupW function (shlwapi.h)
description: UrlFixupW may be altered or unavailable.
helpviewer_keywords: ["UrlFixupW","UrlFixupW function [Windows Shell]","_win32_UrlFixupW","shell.UrlFixupW","shlwapi/UrlFixupW"]
old-location: shell\UrlFixupW.htm
tech.root: shell
ms.assetid: 3750d027-847f-4f33-851d-a10be7562bcb
ms.date: 12/05/2018
ms.keywords: UrlFixupW, UrlFixupW function [Windows Shell], _win32_UrlFixupW, shell.UrlFixupW, shlwapi/UrlFixupW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlFixupW (Unicode)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UrlFixupW
 - shlwapi/UrlFixupW
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
 - UrlFixupW
 - UrlFixupW
---

# UrlFixupW function


## -description

<p class="CCE_Message">[<b>UrlFixupW</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Attempts to correct a URL whose protocol identifier is incorrect. For example, <code>htttp</code> will be changed to <code>http</code>.

## -parameters

### -param pcszUrl [in]

Type: <b>PCWSTR</b>

A pointer to a <b>null</b>-terminated string that contains the URL to be corrected. This string must not exceed INTERNET_MAX_PATH_LENGTH characters in length, including the terminating <b>NULL</b> character.

### -param pszTranslatedUrl [out]

Type: <b>PWSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the copied characters. The buffer must be large enough to contain the number of WCHAR characters specified by the <i>cchMax</i> parameter, including the terminating <b>NULL</b> character. This parameter can be equal to the <i>pcszUrl</i> parameter to correct a URL in place. If <i>pszTranslatedUrl</i> is not equal to <i>pcszUrl</i>, the buffer pointed to by <i>pszTranslatedUrl</i> must not overlap the buffer pointed to by <i>pcszUrl</i>.

### -param cchMax

Type: <b>DWORD</b>

The number of <b>WCHAR</b> characters that can be contained in the buffer pointed to by <i>pszTranslatedUrl</i>. This parameter must be greater than zero.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the proposed URL was already acceptable or was successfully corrected. The <i>pszTranslatedUrl</i> buffer contains the corrected URL, or the original URL if no correction was needed. Returns S_FALSE if the proposed URL could not be recognized sufficiently to be corrected. Otherwise, returns a standard COM error code.

## -remarks

The UrlFixup function recognizes the schemes specified by the <a href="/windows/desktop/api/shlwapi/ne-shlwapi-url_scheme">URL_SCHEME</a> enumeration.

Priority is given to the first character in the protocol identifier section so <code>htp</code> will be converted to <code>http</code> instead of <code>ftp</code>.

<div class="alert"><b>Note</b>  Do not use this function for deterministic data transformation. The heuristics used by <b>UrlFixupW</b> can change from one release to the next. The function should only be used to correct possibly invalid user input.</div>
<div> </div>
This function is available only in a Unicode version.


#### Examples

This example shows how to use <b>UrlFixupW</b>. Notice that the last four autocorrections were probably not what the user intended and demonstrate limitations of the heuristic used by the function.


```cpp

#include <windows.h>
#include <shlwapi.h>
#include <stdio.h>
#include <tchar.h>

void sample(LPCWSTR pszUrl)
{
    WCHAR szBuf[256];
    
    HRESULT hr = UrlFixupW(pszUrl, szBuf, 256);
    if (hr == S_OK) 
    {
        wprintf(L"%-35s %s\n", pszUrl, szBuf);
    } 
    else 
    {
        wprintf(L"%-35s failed\n", pszUrl);
    }
}

int __cdecl main()
{
    sample(L"http://www.microsoft.com");
    sample(L"mail:someone@example.com");
    sample(L"abc:def");
    sample(L"someone@example.com");
    sample(L"htpp:wwwmicrosoft.com");
    sample(L"htps:\\\\www.microsoft.com");
    sample(L"http:someone@example.com");

    return 0;
}

..................................

This example might produce the following output:

http://www.microsoft.com    http://www.microsoft.com
http:www.microsoft.com      http://www.microsoft.com
mail:someone@example.com    mailto:someone@example.com
abc:def                     failed
someone@example.com         failed
htpp:wwwmicrosoft.com       http://wwwmicrosoft.com
htps:\\www.microsoft.com    http://www.microsoft.com
http:someone@example.com    http://someone@example.com
                
```