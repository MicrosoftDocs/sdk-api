---
UID: NF:shlwapi.StrToIntExW
title: StrToIntExW function (shlwapi.h)
description: Converts a string representing a decimal or hexadecimal number to an integer. (Unicode)
helpviewer_keywords: ["STIF_DEFAULT", "STIF_SUPPORT_HEX", "StrToIntEx", "StrToIntEx function [Windows Shell]", "StrToIntExW", "_win32_StrToIntEx", "shell.StrToIntEx", "shlwapi/StrToIntEx", "shlwapi/StrToIntExW"]
old-location: shell\StrToIntEx.htm
tech.root: shell
ms.assetid: 2e8286c7-585f-441b-904b-f3b4e8cf95f9
ms.date: 12/05/2018
ms.keywords: STIF_DEFAULT, STIF_SUPPORT_HEX, StrToIntEx, StrToIntEx function [Windows Shell], StrToIntExA, StrToIntExW, _win32_StrToIntEx, shell.StrToIntEx, shlwapi/StrToIntEx, shlwapi/StrToIntExA, shlwapi/StrToIntExW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrToIntExW (Unicode) and StrToIntExA (ANSI)
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
 - StrToIntExW
 - shlwapi/StrToIntExW
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
 - StrToIntEx
 - StrToIntExA
 - StrToIntExW
---

# StrToIntExW function


## -description

Converts a string representing a decimal or hexadecimal number to an integer.

## -parameters

### -param pszString [in]

Type: <b>PCTSTR</b>

A pointer to the null-terminated string to be converted. For further details concerning the valid forms of the string, see the Remarks section.

### -param dwFlags

Type: <b>STIF_FLAGS</b>

One of the following values that specify how <i>pszString</i> should be parsed for its conversion to an integer.



#### STIF_DEFAULT

The string at <i>pszString</i> contains the representation of a decimal value.



#### STIF_SUPPORT_HEX

The string at <i>pszString</i> contains the representation of either a decimal or hexadecimal value. Note that in hexadecimal representations, the characters A-F are case-insensitive.

### -param piRet [out]

Type: <b>int*</b>

A pointer to an <b>int</b> that receives the converted string. For instance, in the case of the string "123", the integer pointed to by this value receives the integer value 123. 
                    
                    

If this function returns <b>FALSE</b>, this value is undefined.

If the value returned is too large to be contained in a variable of type <b>int</b>, this parameter contains the 32 low-order bits of the value. Any high-order bits beyond that are lost.


##### - dwFlags.STIF_DEFAULT

The string at <i>pszString</i> contains the representation of a decimal value.


##### - dwFlags.STIF_SUPPORT_HEX

The string at <i>pszString</i> contains the representation of either a decimal or hexadecimal value. Note that in hexadecimal representations, the characters A-F are case-insensitive.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the string is converted; otherwise <b>FALSE</b>.

## -remarks

The string pointed to by the <i>pszString</i> parameter must have one of the following forms to be parsed successfully.
                

<ul>
<li>This form is accepted as a decimal value under either flag.
                        
``` syntax
(optional white space)(optional sign)(one or more decimal digits)
```

</li>
<li>These forms are required for hexadecimal values when the STIF_SUPPORT_HEX flag is passed.
                        
``` syntax
(optional white space)(optional sign)0x(one or more hexadecimal digits)
```


``` syntax
(optional white space)(optional sign)0X(one or more hexadecimal digits)
```

</li>
</ul>
The optional sign can be the character '-' or '+'; if omitted, the sign is assumed to be positive.

<div class="alert"><b>Note</b>  If the value is parsed as hexadecimal, the optional sign is ignored, even if it is a '-' character. For example, the string "-0x1" is parsed as 1 instead of -1.</div>
<div> </div>
If the string pointed to by <i>pszString</i> contains an invalid character, that character is considered the end of the string to be converted and the remainder is ignored. For instance, given the invalid hexadecimal string "0x00am123", <b>StrToIntEx</b> only recognizes "0x00a", converts it to the integer value 10, and returns <b>TRUE</b>.




> [!NOTE]
> The shlwapi.h header defines StrToIntEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

