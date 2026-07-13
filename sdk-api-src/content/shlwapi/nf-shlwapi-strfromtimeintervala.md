---
UID: NF:shlwapi.StrFromTimeIntervalA
title: StrFromTimeIntervalA function (shlwapi.h)
description: Converts a time interval, specified in milliseconds, to a string. (ANSI)
helpviewer_keywords: ["StrFromTimeIntervalA", "shlwapi/StrFromTimeIntervalA"]
old-location: shell\StrFromTimeInterval.htm
tech.root: shell
ms.assetid: e2a9492f-acfa-4cbd-8426-895e361f0174
ms.date: 12/05/2018
ms.keywords: StrFromTimeInterval, StrFromTimeInterval function [Windows Shell], StrFromTimeIntervalA, StrFromTimeIntervalW, _win32_StrFromTimeInterval, shell.StrFromTimeInterval, shlwapi/StrFromTimeInterval, shlwapi/StrFromTimeIntervalA, shlwapi/StrFromTimeIntervalW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: StrFromTimeIntervalW (Unicode) and StrFromTimeIntervalA (ANSI)
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
 - StrFromTimeIntervalA
 - shlwapi/StrFromTimeIntervalA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
 - StrFromTimeInterval
 - StrFromTimeIntervalA
 - StrFromTimeIntervalW
---

# StrFromTimeIntervalA function


## -description

Converts a time interval, specified in milliseconds, to a string.

## -parameters

### -param pszOut [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the converted number.

### -param cchMax

Type: <b>UINT</b>

The size of <i>pszOut</i>, in characters. If <i>cchMax</i> is set to zero, <b>StrFromTimeInterval</b> will return the minimum size of the character buffer needed to hold the converted string. In this case, <i>pszOut</i> will not contain the converted string.

### -param dwTimeMS

Type: <b>DWORD</b>

The time interval, in milliseconds.

### -param digits

Type: <b>int</b>

The maximum number of significant digits to be represented in <i>pszOut</i>. Some examples are: 
                
                    


<table class="clsStd">
<tr>
<th>dwTimeMS</th>
<th>digits</th>
<th>pszOut</th>
</tr>
<tr>
<td>34000</td>
<td>3</td>
<td>34 sec</td>
</tr>
<tr>
<td>34000</td>
<td>2</td>
<td>34 sec</td>
</tr>
<tr>
<td>34000</td>
<td>1</td>
<td>30 sec</td>
</tr>
<tr>
<td>74000</td>
<td>3</td>
<td>1 min 14 sec</td>
</tr>
<tr>
<td>74000</td>
<td>2</td>
<td>1 min 10 sec</td>
</tr>
<tr>
<td>74000</td>
<td>1</td>
<td>1 min</td>
</tr>
</table>

## -returns

Type: <b>int</b>

Returns the number of characters in <i>pszOut</i>, excluding the terminating <b>NULL</b> character.

## -remarks

The time value returned in <i>pszOut</i> will always be in the form <i>hh</i> hours <i>mm</i> minutes <i>ss</i> seconds. Times that exceed twenty four hours are not converted to days or months. Fractions of seconds are ignored.


#### Examples


```cpp
#include <windows.h>
#include <iostream.h>
#include "Shlwapi.h"

void main(void)
{
    char TimeString[256];
    char *pszOut;
    pszOut = TimeString;

    cout << "The return value from the call to"
         << "\nthe function StrFromTimeInterval will"
         << "\nreturn the number of elements in the buffer: " << endl;

    cout << "\nThe return from StrFromTimeInterval is " 
         << StrFromTimeInterval(pszOut,30, 34000,30);

    cout << "\nThe contents of the TimeString Buffer " << pszOut << endl;

    cout << "The return from StrFromTimeInterval is " 
         << StrFromTimeInterval(pszOut,30, 74000,3);

    cout << "\nThe contents of the TimeString Buffer " << pszOut << endl;

    cout << "The return from StrFromTimeInterval is " 
         << StrFromTimeInterval(pszOut,30, 74000,2);

    cout << "\nThe contents of the TimeString Buffer " << pszOut << endl;

    cout << "The return from StrFromTimeInterval is " 
         << StrFromTimeInterval(pszOut,30, 74000,1)
         << "\nThe contents of the TimeString Buffer " << pszOut << endl;
}

OUTPUT:
- - - - -
The return value from the call to
the function StrFromTimeInterval will
return the number of elements in the buffer:

The return from StrFromTimeInterval is 7
The contents of the TimeString Buffer  34 sec
The return from StrFromTimeInterval is 13
The contents of the TimeString Buffer  1 min 14 sec
The return from StrFromTimeInterval is 13
The contents of the TimeString Buffer  1 min 10 sec
The return from StrFromTimeInterval is 6
The contents of the TimeString Buffer  1 min
```





> [!NOTE]
> The shlwapi.h header defines StrFromTimeInterval as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

