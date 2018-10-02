---
UID: NF:dbghelp.SymInitializeW
title: SymInitializeW function
author: windows-sdk-content
description: Initializes the symbol handler for a process.
old-location: base\syminitialize.htm
tech.root: debug
ms.assetid: fb1c98cb-6cd0-4218-aea4-384c24c66395
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: SymInitialize, SymInitialize function, SymInitializeW, _win32_syminitialize, base.syminitialize, dbghelp/SymInitialize, dbghelp/SymInitializeW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymInitializeW function


## -description


Initializes the symbol handler for a process.


## -parameters




### -param hProcess [in]

A handle that identifies the caller. This value should be unique and nonzero, but need not be a process handle. However, if you do use a process handle, be sure to use the correct handle. If the application is a debugger, use the process handle for the process being debugged. Do not use the handle returned by <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a> when debugging another process, because calling functions like <a href="https://msdn.microsoft.com/4a880090-f063-4d03-8fd5-a57ccba262c8">SymLoadModuleEx</a> can have unexpected results. 




This parameter cannot be <b>NULL</b>.


### -param UserSearchPath [in, optional]

The path, or series of paths separated by a semicolon (;), that is used to search for symbol files. If this parameter is <b>NULL</b>, the library attempts to form a symbol path from the following sources: 




<ul>
<li>The current working directory of the application</li>
<li>The _NT_SYMBOL_PATH environment variable</li>
<li>The _NT_ALTERNATE_SYMBOL_PATH environment variable</li>
</ul>
Note that the search path can also be set using the <a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a> function.


### -param fInvadeProcess [in]

If this value is <b>TRUE</b>, enumerates the loaded modules for the process and effectively calls the 
<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a> function for each module.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SymInitialize</b> function is used to initialize the symbol handler for a process. In the context of the symbol handler, a process is a convenient object to use when collecting symbol information. Usually, symbol handlers are used by debuggers and other tools that need to load symbols for a process being debugged.

The  handle passed to 
<b>SymInitialize</b> must be the same value passed to all other symbol handler functions called by the process. It is the  handle that the functions use to identify the caller and locate the correct symbol information. When you have finished using the symbol information, call the 
<a href="https://msdn.microsoft.com/56107b71-a3f9-49af-9a90-df3585aed7c8">SymCleanup</a> function to deallocate all resources associated with the process for which symbols are loaded.

The search for symbols files is performed recursively for all paths specified in the <i>UserSearchPath</i> parameter. Therefore, if you specify the root directory in a search, the whole drive is searched, which can take significant time. Note that the directory that contains the executable file for the process is not automatically part of the search path. To include this directory in the search path, call the 
<a href="https://msdn.microsoft.com/4199ce12-e82f-4a58-ac66-e0ddc0dffbff">GetModuleFileNameEx</a> function, then add the path returned to <i>UserSearchPath</i>.

A process that calls <b>SymInitialize</b> should not call it again unless it calls <a href="https://msdn.microsoft.com/56107b71-a3f9-49af-9a90-df3585aed7c8">SymCleanup</a> first. If the call to <b>SymInitialize</b> set <i>fInvadeProcess</i> to <b>TRUE</b> and you simply need to reload the module list, use the <a href="https://msdn.microsoft.com/c1c934e5-4a0a-4cb5-bb12-d6743f034ccb">SymRefreshModuleList</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, call 
<b>SymInitialize</b> only when your process starts and 
<a href="https://msdn.microsoft.com/56107b71-a3f9-49af-9a90-df3585aed7c8">SymCleanup</a> only when your process ends. It is not necessary for each thread in the process to call these functions.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/e8c8f648-c3b0-4595-ac07-f508dd576d9f">Initializing the Symbol Handler</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/4199ce12-e82f-4a58-ac66-e0ddc0dffbff">GetModuleFileNameEx</a>



<a href="https://msdn.microsoft.com/56107b71-a3f9-49af-9a90-df3585aed7c8">SymCleanup</a>



<a href="https://msdn.microsoft.com/281b83ff-8375-4edb-8a10-97af5dbdc87b">SymEnumProcesses</a>



<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a>



<a href="https://msdn.microsoft.com/c1c934e5-4a0a-4cb5-bb12-d6743f034ccb">SymRefreshModuleList</a>



<a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a>
 

 

