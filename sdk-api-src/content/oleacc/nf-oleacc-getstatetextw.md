---
UID: NF:oleacc.GetStateTextW
title: GetStateTextW function (oleacc.h)
description: Retrieves a localized string that describes an object's state for a single predefined state bit flag. Because state values are a combination of one or more bit flags, clients call this function more than once to retrieve all state strings. (Unicode)
helpviewer_keywords: ["GetStateText", "GetStateText function [Windows Accessibility]", "GetStateTextW", "_msaa_GetStateText", "msaa.getstatetext", "oleacc/GetStateText", "oleacc/GetStateTextW", "winauto.getstatetext"]
old-location: winauto\getstatetext.htm
tech.root: WinAuto
ms.assetid: 2a136883-870e-48c3-b182-1cdc64768894
ms.date: 12/05/2018
ms.keywords: GetStateText, GetStateText function [Windows Accessibility], GetStateTextA, GetStateTextW, _msaa_GetStateText, msaa.getstatetext, oleacc/GetStateText, oleacc/GetStateTextA, oleacc/GetStateTextW, winauto.getstatetext
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetStateTextW (Unicode) and GetStateTextA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95
ms.custom: 19H1
f1_keywords:
 - GetStateTextW
 - oleacc/GetStateTextW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
api_name:
 - GetStateText
 - GetStateTextA
 - GetStateTextW
---

# GetStateTextW function


## -description

Retrieves a localized string that describes an object's state for a single predefined state bit flag. Because state values are a combination of one or more bit flags, clients call this function more than once to retrieve all state strings.

## -parameters

### -param lStateBit [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One of the <a href="/windows/desktop/WinAuto/object-state-constants">object state constants</a>.

### -param lpszState [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a buffer that receives the state text string. If this parameter is <b>NULL</b>, the function returns the state string's length, not including the null character.

### -param cchState [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the buffer that is pointed to by the <i>lpszStateBit</i> parameter. For ANSI strings, this value is measured in bytes; for Unicode strings, it is measured in characters.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

If successful, and if <i>lpszStateBit</i> is non-<b>NULL</b>, the return value is the number of bytes (ANSI strings) or characters (Unicode strings) that are copied into the buffer, not including the null-terminated character. If <i>lpszStateBit</i> is <b>NULL</b>, the return value represents the string's length, not including the null character.

If the string resource does not exist, or if the <i>lpszStateBit</i> parameter is not a valid pointer, the return value is zero (0). To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function accepts only one state bit at a time, not a bitmask.




> [!NOTE]
> The oleacc.h header defines GetStateText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
