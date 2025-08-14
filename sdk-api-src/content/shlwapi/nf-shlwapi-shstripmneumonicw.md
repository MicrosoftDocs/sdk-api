---
UID: NF:shlwapi.SHStripMneumonicW
title: SHStripMneumonicW function (shlwapi.h)
description: Removes the mnemonic marker from a string. (Unicode)
helpviewer_keywords: ["SHStripMneumonic", "SHStripMneumonic function [Windows Shell]", "SHStripMneumonicW", "_win32_SHStripMneumonic", "shell.SHStripMneumonic", "shlwapi/SHStripMneumonic", "shlwapi/SHStripMneumonicW"]
old-location: shell\SHStripMneumonic.htm
tech.root: shell
ms.assetid: 25479814-825a-4af2-8751-b35cf39bbb80
ms.date: 12/05/2018
ms.keywords: SHStripMneumonic, SHStripMneumonic function [Windows Shell], SHStripMneumonicA, SHStripMneumonicW, _win32_SHStripMneumonic, shell.SHStripMneumonic, shlwapi/SHStripMneumonic, shlwapi/SHStripMneumonicA, shlwapi/SHStripMneumonicW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHStripMneumonicW (Unicode) and SHStripMneumonicA (ANSI)
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
 - SHStripMneumonicW
 - shlwapi/SHStripMneumonicW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shlwapi-l1-2-1.dll
 - ext-ms-win-shell-shlwapi-l1-2-0.dll
 - Shlwapi.dll
 - API-MS-Win-shlwapi-Winrt-storage-l1-1-0.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - SHStripMneumonic
 - SHStripMneumonicA
 - SHStripMneumonicW
---

# SHStripMneumonicW function


## -description

<p class="CCE_Message">[This function is available through Windows XP and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Removes the mnemonic marker from a string.

## -parameters

### -param pszMenu [in, out]

Type: <b>LPTSTR*</b>

A pointer to the null-terminated string that contains the mnemonic marker.

## -returns

Type: <b>TCHAR</b>

Returns the mnemonic character, if one was found. Otherwise, returns 0.

## -remarks

The term "mnemonic" is misspelled in the function name.

The function supports the following mnemonic formats.
        
                

<table class="clsStd">
<tr>
<th>Input String</th>
<th>Output String</th>
<th>Mnemonic Character</th>
<th>Remarks</th>
</tr>
<tr>
<td>"Str&amp;ing"</td>
<td>"String"</td>
<td>'i'</td>
<td>None.</td>
</tr>
<tr>
<td>"String (&amp;S)"</td>
<td>"String"</td>
<td>'S'</td>
<td>Supported only by the Unicode version of this function. Requires Windows XP or later.</td>
</tr>
</table>
 





> [!NOTE]
> The shlwapi.h header defines SHStripMneumonic as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-drawtext">DrawText</a>
