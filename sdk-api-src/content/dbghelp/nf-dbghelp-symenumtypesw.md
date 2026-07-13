---
UID: NF:dbghelp.SymEnumTypesW
title: SymEnumTypesW function (dbghelp.h)
description: The SymEnumTypesW (Unicode) function enumerates all user-defined types.
helpviewer_keywords: ["SymEnumTypes","SymEnumTypes function","SymEnumTypesW","_win32_symenumtypes","base.symenumtypes","dbghelp/SymEnumTypes","dbghelp/SymEnumTypesW"]
old-location: base\symenumtypes.htm
tech.root: Debug
ms.assetid: 06f964bc-107a-468d-a35d-141b5da1780e
ms.date: 08/04/2022
ms.keywords: SymEnumTypes, SymEnumTypes function, SymEnumTypesW, _win32_symenumtypes, base.symenumtypes, dbghelp/SymEnumTypes, dbghelp/SymEnumTypesW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumTypesW (Unicode) and SymEnumTypes (ANSI)
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
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymEnumTypesW
 - dbghelp/SymEnumTypesW
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
 - SymEnumTypes
 - SymEnumTypes
 - SymEnumTypesW
---

# SymEnumTypesW function


## -description

Enumerates all user-defined types.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param BaseOfDll [in]

The base address of the module.

### -param EnumSymbolsCallback [in]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a> callback function that receives the symbol information.

### -param UserContext [in, optional]

A user-defined value to be passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymEnumTypes as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a>
