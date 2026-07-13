---
UID: NF:shlwapi.IntlStrEqNW
title: IntlStrEqNW macro (shlwapi.h)
description: Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings. (Unicode)
helpviewer_keywords: ["IntlStrEqN", "IntlStrEqN function [Windows Shell]", "IntlStrEqNW", "_win32_IntlStrEqN", "shell.IntlStrEqN", "shlwapi/IntlStrEqN", "shlwapi/IntlStrEqNW"]
old-location: shell\IntlStrEqN.htm
tech.root: shell
ms.assetid: ed777144-398c-4f36-bcc3-f6ba123ebfa7
ms.date: 12/05/2018
ms.keywords: IntlStrEqN, IntlStrEqN function [Windows Shell], IntlStrEqNA, IntlStrEqNW, _win32_IntlStrEqN, shell.IntlStrEqN, shlwapi/IntlStrEqN, shlwapi/IntlStrEqNA, shlwapi/IntlStrEqNW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: IntlStrEqNW (Unicode) and IntlStrEqNA (ANSI)
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
 - IntlStrEqNW
 - shlwapi/IntlStrEqNW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - IntlStrEqN
 - IntlStrEqNA
 - IntlStrEqNW
---

# IntlStrEqNW macro


## -description

Performs a case-sensitive comparison of a specified number of characters from the beginning of two localized strings.

## -parameters

### -param s1 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.

### -param s2 [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string.

### -param nChar [in]

Type: <b>int</b>

The number of characters to be compared, starting from the beginning of the strings.

## -remarks

This function retrieves the thread locale and uses <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw">CompareString</a> to do a case-sensitive comparison of the first <i>nChar</i> characters. It is equivalent to:
				


``` syntax
IntlStrEqWorker(TRUE, pszStr1, pszStr2, nChar)
```





> [!NOTE]
> The shlwapi.h header defines IntlStrEqN as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-intlstreqworkera">IntlStrEqWorker</a>
