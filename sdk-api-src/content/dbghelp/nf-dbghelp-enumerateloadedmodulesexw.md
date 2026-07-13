---
UID: NF:dbghelp.EnumerateLoadedModulesExW
title: EnumerateLoadedModulesExW function (dbghelp.h)
description: The EnumerateLoadedModulesExW (Unicode) function enumerates the loaded modules for the specified process.
helpviewer_keywords: ["EnumerateLoadedModulesEx","EnumerateLoadedModulesEx function","EnumerateLoadedModulesExW","base.enumerateloadedmodulesex","dbghelp/EnumerateLoadedModulesEx","dbghelp/EnumerateLoadedModulesExW"]
old-location: base\enumerateloadedmodulesex.htm
tech.root: Debug
ms.assetid: 4d3d7460-7a84-4d8b-8cea-c6773beac237
ms.date: 08/04/2022
ms.keywords: EnumerateLoadedModulesEx, EnumerateLoadedModulesEx function, EnumerateLoadedModulesExW, base.enumerateloadedmodulesex, dbghelp/EnumerateLoadedModulesEx, dbghelp/EnumerateLoadedModulesExW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumerateLoadedModulesExW (Unicode) and EnumerateLoadedModulesEx (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
f1_keywords:
 - EnumerateLoadedModulesExW
 - dbghelp/EnumerateLoadedModulesExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - EnumerateLoadedModulesEx
 - EnumerateLoadedModulesEx
 - EnumerateLoadedModulesExW
---

# EnumerateLoadedModulesExW function


## -description

Enumerates the loaded modules for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose modules will be enumerated.

### -param EnumLoadedModulesCallback [in]

An application-defined callback function. For more information, see 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-penumloaded_modules_callback">EnumerateLoadedModulesProc64</a>.

### -param UserContext [in, optional]

Optional user-defined data. This value is passed to the callback function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines EnumerateLoadedModulesEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
