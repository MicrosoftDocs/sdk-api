---
UID: NF:dbghelp.SymInitialize
title: SymInitialize function (dbghelp.h)
description: The SymInitialize function (dbghelp.h) initializes the symbol handler for a process.
helpviewer_keywords: ["SymInitialize","SymInitialize function","SymInitializeW","_win32_syminitialize","base.syminitialize","dbghelp/SymInitialize","dbghelp/SymInitializeW"]
old-location: base\syminitialize.htm
tech.root: Debug
ms.assetid: fb1c98cb-6cd0-4218-aea4-384c24c66395
ms.date: 08/04/2022
ms.keywords: SymInitialize, SymInitialize function, SymInitializeW, _win32_syminitialize, base.syminitialize, dbghelp/SymInitialize, dbghelp/SymInitializeW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymInitializeW (Unicode) and SymInitialize (ANSI)
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
 - SymInitialize
 - dbghelp/SymInitialize
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
 - SymInitialize
 - SymInitialize
 - SymInitializeW
---

# SymInitialize function


## -description

Initializes the symbol handler for a process.

## -parameters

### -param hProcess [in]

A handle that identifies the caller. This value should be unique and nonzero, but need not be a process handle. However, if you do use a process handle, be sure to use the correct handle. If the application is a debugger, use the process handle for the process being debugged. Do not use the handle returned by <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a>. The handle used must be unique to avoid sharing a session with another component, and using <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> can have unexpected results when multiple components are attempting to use dbghelp to inspect the current process. Using <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess">GetCurrentProcess</a> when debugging another process will also cause functions like <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmoduleex">SymLoadModuleEx</a> to have unexpected results.




This parameter cannot be <b>NULL</b>.

### -param UserSearchPath [in, optional]

The path, or series of paths separated by a semicolon (;), that is used to search for symbol files. If this parameter is <b>NULL</b>, the library attempts to form a symbol path from the following sources: 




<ul>
<li>The current working directory of the application</li>
<li>The _NT_SYMBOL_PATH environment variable</li>
<li>The _NT_ALTERNATE_SYMBOL_PATH environment variable</li>
</ul>
Note that the search path can also be set using the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.

### -param fInvadeProcess [in]

If this value is <b>TRUE</b>, enumerates the loaded modules for the process and effectively calls the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a> function for each module.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymInitialize</b> function is used to initialize the symbol handler for a process. In the context of the symbol handler, a process is a convenient object to use when collecting symbol information. Usually, symbol handlers are used by debuggers and other tools that need to load symbols for a process being debugged.

The  handle passed to 
<b>SymInitialize</b> must be the same value passed to all other symbol handler functions called by the process. It is the  handle that the functions use to identify the caller and locate the correct symbol information. When you have finished using the symbol information, call the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symcleanup">SymCleanup</a> function to deallocate all resources associated with the process for which symbols are loaded.

The search for symbols files is performed recursively for all paths specified in the <i>UserSearchPath</i> parameter. Therefore, if you specify the root directory in a search, the whole drive is searched, which can take significant time. Note that the directory that contains the executable file for the process is not automatically part of the search path. To include this directory in the search path, call the 
<a href="/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa">GetModuleFileNameEx</a> function, then add the path returned to <i>UserSearchPath</i>.

A process that calls <b>SymInitialize</b> should not call it again unless it calls <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symcleanup">SymCleanup</a> first. If the call to <b>SymInitialize</b> set <i>fInvadeProcess</i> to <b>TRUE</b> and you simply need to reload the module list, use the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symrefreshmodulelist">SymRefreshModuleList</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, call 
<b>SymInitialize</b> only when your process starts and 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symcleanup">SymCleanup</a> only when your process ends. It is not necessary for each thread in the process to call these functions.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/initializing-the-symbol-handler">Initializing the Symbol Handler</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa">GetModuleFileNameEx</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symcleanup">SymCleanup</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumprocesses">SymEnumProcesses</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symloadmodule">SymLoadModule64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symrefreshmodulelist">SymRefreshModuleList</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a>
