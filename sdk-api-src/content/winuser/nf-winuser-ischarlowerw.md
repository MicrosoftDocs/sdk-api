---
UID: NF:winuser.IsCharLowerW
title: IsCharLowerW
description: The IsCharLowerW (Unicode) function determines whether a character is lowercase. (IsCharLowerW)
ms.date: 08/02/2022
ms.keywords: IsCharLowerW
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: winuser.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - IsCharLowerW
 - winuser/IsCharLowerW
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-string-l2-1-1.dll
 - api-ms-win-core-string-l2-1-0.dll
 - User32.dll
 - API-MS-Win-Core-Stringansi-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-user32-l1-1-0.dll
 - API-MS-Win-DownLevel-user32-l1-1-1.dll
 - mfc120u.dll mfc140u.dll
api_name:
 - IsCharLowerW
---

## -description

Determines whether a character is lowercase. This determination is based on the semantics of the language selected by the user during setup or through Control Panel.

## -parameters

### -param ch

Type: <b>WCHAR</b>

The character to be tested.

## -returns

Type: <b>BOOL</b>

If the character is lowercase, the return value is nonzero.

If the character is not lowercase, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

> [!NOTE]
> The winuser.h header defines IsCharLower as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-ischaruppera">IsCharUpper</a>



<b>Reference</b>



<a href="/windows/desktop/menurc/strings">Strings</a>
