---
UID: NF:dbghelp.SymLoadModule64
title: SymLoadModule64 function
author: windows-sdk-content
description: Loads the symbol table.
old-location: base\symloadmodule64.htm
tech.root: debug
ms.assetid: be50588b-066b-42ab-ba81-7537c811676f
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: SymLoadModule, SymLoadModule function, SymLoadModule64, SymLoadModule64 function, _win32_symloadmodule64, base.symloadmodule64, dbghelp/SymLoadModule, dbghelp/SymLoadModule64
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
req.unicode-ansi: 
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
 - SymLoadModule64
 - SymLoadModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymLoadModule64 function


## -description


Loads the symbol table.

This function has been superseded by the <a href="https://msdn.microsoft.com/4a880090-f063-4d03-8fd5-a57ccba262c8">SymLoadModuleEx</a> function.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have been previously passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param hFile [in, optional]

A handle to the file for the executable image. This argument is used mostly by debuggers, where the debugger passes the file handle obtained from a debugging event. A value of <b>NULL</b> indicates that <i>hFile</i> is not used.


### -param ImageName [in, optional]

The name of the executable image. This name can contain a partial path, a full path, or no path at all. If the file cannot be located by the name provided, the symbol search path is used.


### -param ModuleName [in, optional]

A shortcut name for the module. If the pointer value is <b>NULL</b>, the library creates a name using the base name of the symbol file.


### -param BaseOfDll [in]

The load address of the module. If the value is zero, the library obtains the load address from the symbol file. The load address contained in the symbol file is not necessarily the actual load address. Debuggers and other applications having an actual load address should use the real load address when calling this function.

If the image is a .pdb file, this parameter cannot be zero.


### -param SizeOfDll [in]

The size of the module, in bytes. If the value is zero, the library obtains the size from the symbol file. The size contained in the symbol file is not necessarily the actual size. Debuggers and other applications having an actual size should use the real size when calling this function.

If the image is a .pdb file, this parameter cannot be zero.


## -returns



If the function succeeds, the return value is the base address of the loaded module.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the module is already loaded, the return value is zero and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_SUCCESS</b>.




## -remarks



The symbol handler creates an entry for the module and if the deferred symbol loading option is turned off, an attempt is made to load the symbols. If deferred symbol loading is enabled, the module is marked as deferred and the symbols are not loaded until a reference is made to a symbol in the module.

To unload the symbol table, use the 
<a href="https://msdn.microsoft.com/f4801039-eba2-4ec3-8c23-706ab89bb442">SymUnloadModule64</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymLoadModule</b> function. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>SymLoadModule</b> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymLoadModule SymLoadModule64
#else
DWORD
IMAGEAPI
SymLoadModule(
    __in HANDLE hProcess,
    __in_opt HANDLE hFile,
    __in_opt PCSTR ImageName,
    __in_opt PCSTR ModuleName,
    __in DWORD BaseOfDll,
    __in DWORD SizeOfDll
    );
#endif
```





## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>



<a href="https://msdn.microsoft.com/f4801039-eba2-4ec3-8c23-706ab89bb442">SymUnloadModule64</a>
 

 

