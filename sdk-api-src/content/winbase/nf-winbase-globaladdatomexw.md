---
UID: NF:winbase.GlobalAddAtomExW
title: GlobalAddAtomExW function (winbase.h)
description: Adds a character string to the global atom table and returns a unique value (an atom) identifying the string. (GlobalAddAtomExW)
helpviewer_keywords: ["GlobalAddAtomEx", "GlobalAddAtomEx function [Data Exchange]", "GlobalAddAtomExW", "dataxchg.globaladdatomex", "winbase/GlobalAddAtomEx", "winbase/GlobalAddAtomExW"]
old-location: dataxchg\globaladdatomex.htm
tech.root: dataxchg
ms.assetid: C5D982F5-94A9-4B08-AE07-8F40E4128123
ms.date: 12/05/2018
ms.keywords: GlobalAddAtomEx, GlobalAddAtomEx function [Data Exchange], GlobalAddAtomExA, GlobalAddAtomExW, dataxchg.globaladdatomex, winbase/GlobalAddAtomEx, winbase/GlobalAddAtomExA, winbase/GlobalAddAtomExW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GlobalAddAtomExW (Unicode) and GlobalAddAtomExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GlobalAddAtomExW
 - winbase/GlobalAddAtomExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-atoms-l1-1-0.dll
 - Kernel32.dll
api_name:
 - GlobalAddAtomEx
 - GlobalAddAtomExA
 - GlobalAddAtomExW
---

# GlobalAddAtomExW function


## -description

Adds a character string to the global atom table and returns a unique value (an atom) identifying the string.

## -parameters

### -param lpString [in, optional]

The null-terminated string to be added. The string can have a maximum size of 255 bytes. Strings that differ only in case are considered identical. The case of the first string of this name added to the table is preserved and returned by the <a href="/windows/win32/api/winbase/nf-winbase-globalgetatomnamea">GlobalGetAtomName</a> function.

Alternatively, you can use an integer atom that has been converted using the <a href="/windows/win32/api/winbase/nf-winbase-makeintatom">MAKEINTATOM</a> macro. See the Remarks for more information.

### -param Flags [in]

## -returns

If the function succeeds, the return value is the newly created atom.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/win32/api/winbase/nf-winbase-globaladdatoma">GlobalAddAtom</a>

## -remarks

> [!NOTE]
> The winbase.h header defines GlobalAddAtomEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
