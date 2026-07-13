---
UID: NF:shlwapi.StrToIntA
title: StrToIntA function (shlwapi.h)
description: Converts a string that represents a decimal value to an integer. The StrToLong macro is identical to this function. (ANSI)
helpviewer_keywords: ["StrToIntA", "shlwapi/StrToIntA"]
old-location: shell\StrToInt.htm
tech.root: shell
ms.assetid: 74313e56-a820-4d02-91f4-f629d2fc72d4
ms.date: 12/05/2018
ms.keywords: StrToInt, StrToInt function [Windows Shell], StrToIntA, StrToIntW, _win32_StrToInt, shell.StrToInt, shlwapi/StrToInt, shlwapi/StrToIntA, shlwapi/StrToIntW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrToIntW (Unicode) and StrToIntA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StrToIntA
 - shlwapi/StrToIntA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-shlwapi-Obsolete-l1-2-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
 - API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
 - StrToInt
 - StrToIntA
 - StrToIntW
---

# StrToIntA function


## -description

Converts a string that represents a decimal value to an integer. The <b>StrToLong</b> macro is identical to this function.

## -parameters

### -param pszSrc [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated string to be converted. A valid string representing a decimal value contains only the characters 0-9 and must have the following form to be parsed successfully.
                    
                    


``` syntax
(optional white space)(optional sign)(one or more decimal digits)
```

The optional sign can be the character '-' or '+'; if omitted, the sign is assumed to be positive.

## -returns

Type: <b>int</b>

Returns the <b>int</b> value represented by <i>pszSrc</i>. For instance, the string "123" returns the integer value 123.

## -remarks

If the string pointed to by <i>pszSrc</i> contains an invalid character, that character is considered the end of the string to be converted and the remainder is ignored. For instance, given the invalid decimal string "12b34", <b>StrToInt</b> only recognizes "12" and returns that integer value.





> [!NOTE]
> The shlwapi.h header defines StrToInt as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-strtointexa">StrToIntEx</a>
