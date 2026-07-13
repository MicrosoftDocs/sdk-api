---
UID: NF:shlwapi.ParseURLA
title: ParseURLA function (shlwapi.h)
description: Performs rudimentary parsing of a URL. (ANSI)
helpviewer_keywords: ["ParseURLA", "shlwapi/ParseURLA"]
old-location: shell\ParseURL.htm
tech.root: shell
ms.assetid: 3d42dad0-b9eb-4e40-afc8-68cb85b27504
ms.date: 12/05/2018
ms.keywords: ParseURL, ParseURL function [Windows Shell], ParseURLA, ParseURLW, _win32_ParseURL, shell.ParseURL, shlwapi/ParseURL, shlwapi/ParseURLA, shlwapi/ParseURLW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ParseURLW (Unicode) and ParseURLA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 6.0.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ParseURLA
 - shlwapi/ParseURLA
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
 - ParseURL
 - ParseURLA
 - ParseURLW
---

# ParseURLA function


## -description

Performs rudimentary parsing of a URL.

## -parameters

### -param pcszURL [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string containing the URL to be parsed.

### -param ppu [in, out]

Type: <b><a href="/windows/desktop/api/shlwapi/ns-shlwapi-parsedurla">PARSEDURL</a>*</b>

A pointer to a <a href="/windows/desktop/api/shlwapi/ns-shlwapi-parsedurla">PARSEDURL</a> structure that receives the parsed results. The calling application must set the structure's <i>cbSize</i> member to the size of the structure before calling <b>ParseURL</b>.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> on success, or a COM error code otherwise. The function returns <b>URL_E_INVALID_SYNTAX</b> (defined in Intshcut.h) if the string could not be parsed as a URL.

## -remarks

The parsing performed by <b>ParseURL</b> is fairly rudimentary. For more sophisticated URL parsing, use <a href="/windows/desktop/api/wininet/nf-wininet-internetcrackurla">InternetCrackUrl</a>.


#### Examples

This sample console application uses <b>ParseURL</b> to parse several simple URLs.


```cpp

#include <windows.h>
#include <shlwapi.h>
#include <stdio.h>
#include <tchar.h>

void sample(LPCTSTR pcszUrl)
{
    PARSEDURL pu;
    pu.cbSize = sizeof(pu);
    HRESULT hr = ParseURL(pcszUrl, &pu);
    _tprintf(TEXT("ParseURL(%s) returned 0x%08x\n"), pcszUrl, hr);
    if (SUCCEEDED(hr)) {
        _tprintf(TEXT("Protocol = %.*s\n"), pu.cchProtocol, pu.pszProtocol);
        _tprintf(TEXT("Suffix   = %.*s\n"), pu.cchSuffix, pu.pszSuffix);
        _tprintf(TEXT("Scheme   = %d\n"), pu.nScheme);
        _tprintf(TEXT("\n"));
    }
}

int __cdecl main()
{
    sample(TEXT("http://msdn.microsoft.com/vstudio/"));
    sample(TEXT("mailto:someone@example.com"));
    sample(TEXT("file://C:\\AUTOEXEC.BAT"));
    sample(TEXT("C:\\AUTOEXEC.BAT"));
    return 0;
}   

OUTPUT:
---------

ParseURL(http://msdn.microsoft.com/vstudio/) returned 0x00000000
Protocol = http
Suffix   = //msdn.microsoft.com/vstudio/
Scheme   = 2

ParseURL(mailto:someone@example.com) returned 0x00000000
Protocol = mailto
Suffix   = someone@example.com
Scheme   = 4

ParseURL(file://C:\AUTOEXEC.BAT) returned 0x00000000
Protocol = file
Suffix   = C:\AUTOEXEC.BAT
Scheme   = 9

ParseURL(C:\AUTOEXEC.BAT) returned 0x80041001
                
```





> [!NOTE]
> The shlwapi.h header defines ParseURL as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
