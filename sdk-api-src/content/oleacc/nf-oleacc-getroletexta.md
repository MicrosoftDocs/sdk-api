---
UID: NF:oleacc.GetRoleTextA
title: GetRoleTextA function (oleacc.h)
description: Retrieves the localized string that describes the object's role for the specified role value. (ANSI)
helpviewer_keywords: ["GetRoleTextA", "oleacc/GetRoleTextA"]
old-location: winauto\getroletext.htm
tech.root: WinAuto
ms.assetid: 58436001-92d7-4afa-af07-169c8bbda9ba
ms.date: 12/05/2018
ms.keywords: GetRoleText, GetRoleText function [Windows Accessibility], GetRoleTextA, GetRoleTextW, _msaa_GetRoleText, msaa.getroletext, oleacc/GetRoleText, oleacc/GetRoleTextA, oleacc/GetRoleTextW, winauto.getroletext
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetRoleTextW (Unicode) and GetRoleTextA (ANSI)
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
 - GetRoleTextA
 - oleacc/GetRoleTextA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleacc.dll
 - ext-ms-win-oleacc-l1-1-1.dll
api_name:
 - GetRoleText
 - GetRoleTextA
 - GetRoleTextW
---

# GetRoleTextA function


## -description

Retrieves the localized string that describes the object's role for the specified role value.

## -parameters

### -param lRole [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One of the <a href="/windows/desktop/WinAuto/object-roles">object role</a> constants.

### -param lpszRole [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Address of a buffer that receives the role text string. If this parameter is <b>NULL</b>, the function returns the role string's length, not including the null character.

### -param cchRoleMax [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the buffer that is pointed to by the <i>lpszRole</i> parameter. For ANSI strings, this value is measured in bytes; for Unicode strings, it is measured in characters.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

If successful, and if <i>lpszRole</i> is non-<b>NULL</b>, the return value is the number of bytes (ANSI strings) or characters (Unicode strings) copied into the buffer, not including the terminating null character. If <i>lpszRole</i> is <b>NULL</b>, the return value represents the string's length, not including the null character.

If the string resource does not exist, or if the <i>lpszRole</i> parameter is not a valid pointer, the return value is zero (0). To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

> [!NOTE]
> The oleacc.h header defines GetRoleText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
