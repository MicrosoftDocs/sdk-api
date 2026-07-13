---
UID: NF:ras.RasValidateEntryNameA
title: RasValidateEntryNameA function (ras.h)
description: The RasValidateEntryName function validates the format of a connection entry name. The name must contain at least one non-white-space alphanumeric character. (ANSI)
helpviewer_keywords: ["RasValidateEntryNameA", "ras/RasValidateEntryNameA"]
old-location: rras\rasvalidateentryname.htm
tech.root: RRAS
ms.assetid: c70ad0d4-6bc1-4716-9a8e-0fbeb55b7560
ms.date: 12/05/2018
ms.keywords: RasValidateEntryName, RasValidateEntryName function [RAS], RasValidateEntryNameA, RasValidateEntryNameW, _ras_rasvalidateentryname, ras/RasValidateEntryName, ras/RasValidateEntryNameA, ras/RasValidateEntryNameW, rras.rasvalidateentryname
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasValidateEntryNameW (Unicode) and RasValidateEntryNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasValidateEntryNameA
 - ras/RasValidateEntryNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
api_name:
 - RasValidateEntryName
 - RasValidateEntryNameA
 - RasValidateEntryNameW
---

# RasValidateEntryNameA function


## -description

The 
<b>RasValidateEntryName</b> function validates the format of a connection entry name. The name must contain at least one non-white-space alphanumeric character.

## -parameters

### -param unnamedParam1 [in]

A pointer to a null-terminated string that specifies the full path and file name of a phone-book (PBK) file. If this parameter is <b>NULL</b>, the function uses the current default phone-book file. 




<b>Windows Me/98/95:  </b>This parameter should always be <b>NULL</b>. Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.

### -param unnamedParam2 [in]

Pointer to a null-terminated string that specifies an entry name. 




The following characters are not allowed in an entry name.

<table>
<tr>
<th>Character</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="_"></a><dl>
<dt><b>|</b></dt>
</dl>
</td>
<td width="60%">
vertical bar

</td>
</tr>
<tr>
<td width="40%"><a id="_"></a><dl>
<dt><b>&gt;</b></dt>
</dl>
</td>
<td width="60%">
greater than symbol

</td>
</tr>
<tr>
<td width="40%"><a id="_"></a><dl>
<dt><b>&lt;</b></dt>
</dl>
</td>
<td width="60%">
less than symbol

</td>
</tr>
<tr>
<td width="40%"><a id="__"></a><dl>
<dt><b>? </b></dt>
</dl>
</td>
<td width="60%">
question mark

</td>
</tr>
<tr>
<td width="40%"><a id="_"></a><dl>
<dt><b>*</b></dt>
</dl>
</td>
<td width="60%">
asterisk

</td>
</tr>
<tr>
<td width="40%"><a id="_"></a><dl>
<dt><b>\</b></dt>
</dl>
</td>
<td width="60%">
backward slash

</td>
</tr>
<tr>
<td width="40%"><a id="_"></a><dl>
<dt><b>/</b></dt>
</dl>
</td>
<td width="60%">
forward slash

</td>
</tr>
<tr>
<td width="40%"><a id="__"></a><dl>
<dt><b>: </b></dt>
</dl>
</td>
<td width="60%">
colon

</td>
</tr>
</table>
 

<b>Windows 2000 or later:  </b>The entry name cannot begin with a period (".").

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
The entry name already exists in the specified phonebook.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK</b></dt>
</dl>
</td>
<td width="60%">
The specified phonebook doesn't exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The format of the specified entry name is invalid.

</td>
</tr>
</table>

## -remarks

The following sample code validates the phone-book entry specified by the variable <i>lpszEntry</i>.


```cpp
#include <windows.h>
#include <stdio.h>
#include "ras.h"
#include <tchar.h>

DWORD __cdecl wmain(){

    LPTSTR lpszEntry = L"EntryName\0";

    DWORD nRet = RasValidateEntryName(NULL, lpszEntry);

    switch (nRet)
    {
        case ERROR_SUCCESS:
            printf("Entry name: %s is valid but doesn't exist in the default phone book\n", lpszEntry);
            break;
        case ERROR_INVALID_NAME:
            printf("Entry name: %s is invalid\n", lpszEntry);
            break;
        case ERROR_ALREADY_EXISTS:
            printf("Entry name: %s already exists in the default phone book\n", lpszEntry);
            break;
        default:
            printf("RasValidateEntryName failed: Error = %d\n", nRet);
            break;
    }
}

```






> [!NOTE]
> The ras.h header defines RasValidateEntryName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ras/nf-ras-rascreatephonebookentrya">RasCreatePhonebookEntry</a>



<a href="/windows/desktop/api/ras/nf-ras-rasgetentrypropertiesa">RasGetEntryProperties</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
