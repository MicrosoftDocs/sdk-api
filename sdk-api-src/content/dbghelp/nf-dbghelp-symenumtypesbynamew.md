---
UID: NF:dbghelp.SymEnumTypesByNameW
title: SymEnumTypesByNameW function (dbghelp.h)
description: Enumerates all user-defined types.
helpviewer_keywords: ["SymEnumTypesByName","SymEnumTypesByName function","SymEnumTypesByNameW","base.symenumtypesbyname","dbghelp/SymEnumTypesByName","dbghelp/SymEnumTypesByNameW"]
old-location: base\symenumtypesbyname.htm
tech.root: Debug
ms.assetid: 48acb588-23fa-44f3-8b8c-f3c76371d1fd
ms.date: 12/05/2018
ms.keywords: SymEnumTypesByName, SymEnumTypesByName function, SymEnumTypesByNameW, base.symenumtypesbyname, dbghelp/SymEnumTypesByName, dbghelp/SymEnumTypesByNameW
f1_keywords:
- dbghelp/SymEnumTypesByName
dev_langs:
- c++
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymEnumTypesByNameW (Unicode) and SymEnumTypesByName (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dbghelp.dll
- imagehlp.dll
api_name:
- SymEnumTypesByName
- SymEnumTypesByName
- SymEnumTypesByNameW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
---

# SymEnumTypesByNameW function


## -description


Enumerates all user-defined types.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param BaseOfDll [in]

The base address of the module.


### -param mask [in, optional]

A wildcard expression that indicates the names of the symbols to be enumerated. To specify a module name, use the !<i>mod</i> syntax.


### -param EnumSymbolsCallback [in]

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a> callback function that receives the symbol information.


### -param UserContext [in]

A user-defined value to be passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymEnumTypesByName as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumeratesymbols_callback">SymEnumSymbolsProc</a>
 

 

