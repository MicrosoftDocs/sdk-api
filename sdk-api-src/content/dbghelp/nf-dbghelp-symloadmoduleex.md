---
UID: NF:dbghelp.SymLoadModuleEx
title: SymLoadModuleEx function
author: windows-sdk-content
description: Loads the symbol table for the specified module.
old-location: base\symloadmoduleex.htm
old-project: debug
ms.assetid: 4a880090-f063-4d03-8fd5-a57ccba262c8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SLMFLAG_NO_SYMBOLS, SLMFLAG_VIRTUAL, SymLoadModuleEx, SymLoadModuleEx function, SymLoadModuleExW, _win32_symloadmoduleex, base.symloadmoduleex, dbghelp/SymLoadModuleEx, dbghelp/SymLoadModuleExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 6.0 or later
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymLoadModuleExW (Unicode) and SymLoadModuleEx (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymLoadModuleEx
 - SymLoadModuleEx
 - SymLoadModuleExW
product: Windows
targetos: Windows
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
---

# SymLoadModuleEx function


## -description


Loads the symbol table for the specified module.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param hFile [in]

A handle to the file for the executable image. This argument is used mostly by debuggers, where the debugger passes the file handle obtained from a debugging event. A value of <b>NULL</b> indicates that <i>hFile</i> is not used.


### -param ImageName [in]

The name of the executable image. This name can contain a partial path, a full path, or no path at all. If the file cannot be located by the name provided, the symbol search path is used.


### -param ModuleName [in]

A shortcut name for the module. If the pointer value is <b>NULL</b>, the library creates a name using the base name of the symbol file.


### -param BaseOfDll [in]

The load address of the module. If the value is zero, the library obtains the load address from the symbol file. The load address contained in the symbol file is not necessarily the actual load address. Debuggers and other applications having an actual load address should use the real load address when calling this function.

If the image is a .pdb file, this parameter cannot be zero.


### -param DllSize [in]

The size of the module, in bytes. If the value is zero, the library obtains the size from the symbol file. The size contained in the symbol file is not necessarily the actual size. Debuggers and other applications having an actual size should use the real size when calling this function.

If the image is a .pdb file, this parameter cannot be zero.


### -param Data [in]

A pointer to a 
<a href="https://msdn.microsoft.com/aa9c2b18-01bf-4eaa-8283-584ca16fc98e">MODLOAD_DATA</a> structure that represents headers other than the standard PE header. This parameter is optional and can be <b>NULL</b>.


### -param Flags [in]

This parameter can be zero or one or more of the following values. If this parameter is zero, the function loads the modules and the symbols for the module.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SLMFLAG_NO_SYMBOLS"></a><a id="slmflag_no_symbols"></a><dl>
<dt><b>SLMFLAG_NO_SYMBOLS</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
Loads the module but not the symbols for the module.

</td>
</tr>
<tr>
<td width="40%"><a id="SLMFLAG_VIRTUAL"></a><a id="slmflag_virtual"></a><dl>
<dt><b>SLMFLAG_VIRTUAL</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Creates a virtual module named <i>ModuleName</i> at the address specified in <i>BaseOfDll</i>. To add symbols to this module, call the 
<a href="https://msdn.microsoft.com/28405993-035f-4946-91c3-0e3e34fd8824">SymAddSymbol</a> function.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is the base address of the loaded module.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the module is already loaded, the return value is zero and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_SUCCESS.




## -remarks



The symbol handler creates an entry for the module and if the deferred symbol loading option is turned off, an attempt is made to load the symbols. If deferred symbol loading is enabled, the module is marked as deferred and the symbols are not loaded until a reference is made to a symbol in the module. Therefore, you should always call the <a href="https://msdn.microsoft.com/e8057cb5-3331-4460-b07c-4338a57024be">SymGetModuleInfo64</a> function after calling <b>SymLoadModuleEx</b>.

To unload the symbol table, use the 
<a href="https://msdn.microsoft.com/f4801039-eba2-4ec3-8c23-706ab89bb442">SymUnloadModule64</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/01cee812-d1f2-4459-acee-bce8719a85b2">Loading a Symbol Module</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/aa9c2b18-01bf-4eaa-8283-584ca16fc98e">MODLOAD_DATA</a>



<a href="https://msdn.microsoft.com/28405993-035f-4946-91c3-0e3e34fd8824">SymAddSymbol</a>



<a href="https://msdn.microsoft.com/f4801039-eba2-4ec3-8c23-706ab89bb442">SymUnloadModule64</a>
 

 

