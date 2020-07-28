---
UID: NF:dbghelp.SymEnumSourceFiles
title: SymEnumSourceFiles function (dbghelp.h)
description: Enumerates all source files in a process.
helpviewer_keywords: ["SymEnumSourceFiles","SymEnumSourceFiles function","SymEnumSourceFilesW","base.symenumsourcefiles","dbghelp/SymEnumSourceFiles","dbghelp/SymEnumSourceFilesW"]
old-location: base\symenumsourcefiles.htm
tech.root: Debug
ms.assetid: 4649bdc6-74c5-4529-bedc-64e0277144d0
ms.date: 12/05/2018
ms.keywords: SymEnumSourceFiles, SymEnumSourceFiles function, SymEnumSourceFilesW, base.symenumsourcefiles, dbghelp/SymEnumSourceFiles, dbghelp/SymEnumSourceFilesW
f1_keywords:
- dbghelp/SymEnumSourceFiles
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
req.unicode-ansi: SymEnumSourceFilesW (Unicode) and SymEnumSourceFiles (ANSI)
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
- SymEnumSourceFiles
- SymEnumSourceFiles
- SymEnumSourceFilesW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# SymEnumSourceFiles function


## -description


Enumerates all source files in a process.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param ModBase [in]

The base address of the module. If this value is zero and <i>Mask</i> contains an exclamation point (!), the function looks across modules. If this value is zero and <i>Mask</i> does not contain an exclamation point, the function uses the scope established by the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symsetcontext">SymSetContext</a> function.


### -param Mask [in, optional]

A wildcard expression that indicates the names of the source files to be enumerated. To specify a module name, use the !<i>mod</i> syntax.

If this parameter is <b>NULL</b>, the function will enumerate all files.


### -param cbSrcFiles [in]

Pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumsourcefiles_callback">SymEnumSourceFilesProc</a> callback function that receives the source file information.


### -param UserContext [in, optional]

User-defined value that is passed to the callback function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context for the callback function.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumsourcefiles_callback">SymEnumSourceFilesProc</a>
 

 

