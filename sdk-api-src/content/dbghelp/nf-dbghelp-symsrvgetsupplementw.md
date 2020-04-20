---
UID: NF:dbghelp.SymSrvGetSupplementW
title: SymSrvGetSupplementW function (dbghelp.h)
description: Retrieves the specified file from the supplement for a symbol store.helpviewer_keywords: ["SymSrvGetSupplement","SymSrvGetSupplement function","SymSrvGetSupplementW","base.symsrvgetsupplement","dbghelp/SymSrvGetSupplement","dbghelp/SymSrvGetSupplementW"]
old-location: base\symsrvgetsupplement.htm
tech.root: Debug
ms.assetid: 2cad61c6-c8a1-437f-8e2c-1fa70eb348c2
ms.date: 12/05/2018
ms.keywords: SymSrvGetSupplement, SymSrvGetSupplement function, SymSrvGetSupplementW, base.symsrvgetsupplement, dbghelp/SymSrvGetSupplement, dbghelp/SymSrvGetSupplementW
f1_keywords:
- dbghelp/SymSrvGetSupplement
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
req.unicode-ansi: SymSrvGetSupplementW (Unicode) and SymSrvGetSupplement (ANSI)
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
api_name:
- SymSrvGetSupplement
- SymSrvGetSupplement
- SymSrvGetSupplementW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
---

# SymSrvGetSupplementW function


## -description


Retrieves the specified file from the supplement for a symbol store.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param SymPath [in, optional]

The symbol path. The function uses only the symbol stores described in standard syntax for symbol stores. All other paths are ignored. If this parameter is <b>NULL</b>, the function uses the symbol path set using the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> or <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.


### -param Node [in]

The symbol file associated with the supplemental file.


### -param File [in]

The name of the file.


## -returns



If the function succeeds, the return value is the fully qualified path for the supplemental file.
						

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



For more information on supplemental files, see <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symsrvstoresupplement">SymSrvStoreSupplement</a>.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symsrvstoresupplement">SymSrvStoreSupplement</a>
 

 

