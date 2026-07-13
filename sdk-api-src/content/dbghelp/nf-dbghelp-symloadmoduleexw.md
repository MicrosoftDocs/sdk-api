---
UID: NF:dbghelp.SymLoadModuleExW
title: SymLoadModuleExW function (dbghelp.h)
description: The SymLoadModuleExW (Unicode) function loads the symbol table for the specified module.
helpviewer_keywords: ["SLMFLAG_NO_SYMBOLS","SLMFLAG_VIRTUAL","SymLoadModuleEx","SymLoadModuleEx function","SymLoadModuleExW","_win32_symloadmoduleex","base.symloadmoduleex","dbghelp/SymLoadModuleEx","dbghelp/SymLoadModuleExW"]
old-location: base\symloadmoduleex.htm
tech.root: Debug
ms.assetid: 4a880090-f063-4d03-8fd5-a57ccba262c8
ms.date: 08/04/2022
ms.keywords: SLMFLAG_NO_SYMBOLS, SLMFLAG_VIRTUAL, SymLoadModuleEx, SymLoadModuleEx function, SymLoadModuleExW, _win32_symloadmoduleex, base.symloadmoduleex, dbghelp/SymLoadModuleEx, dbghelp/SymLoadModuleExW
req.header: dbghelp.h
req.include-header: 
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
f1_keywords:
 - SymLoadModuleExW
 - dbghelp/SymLoadModuleExW
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
 - SymLoadModuleEx
 - SymLoadModuleEx
 - SymLoadModuleExW
---

# SymLoadModuleExW function


## -description

Loads the symbol table for the specified module.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

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
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-modload_data">MODLOAD_DATA</a> structure that represents headers other than the standard PE header. This parameter is optional and can be <b>NULL</b>.

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
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symaddsymbol">SymAddSymbol</a> function.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the base address of the loaded module.

If the function fails, the return value is zero. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the module is already loaded, the return value is zero and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_SUCCESS.

## -remarks

The symbol handler creates an entry for the module and if the deferred symbol loading option is turned off, an attempt is made to load the symbols. If deferred symbol loading is enabled, the module is marked as deferred and the symbols are not loaded until a reference is made to a symbol in the module. Therefore, you should always call the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetmoduleinfo64">SymGetModuleInfo64</a> function after calling <b>SymLoadModuleEx</b>.

To unload the symbol table, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symunloadmodule64">SymUnloadModule64</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/loading-a-symbol-module">Loading a Symbol Module</a>.

<div class="code"></div>




> [!NOTE]
> The dbghelp.h header defines SymLoadModuleEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-modload_data">MODLOAD_DATA</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symaddsymbol">SymAddSymbol</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symunloadmodule">SymUnloadModule64</a>
