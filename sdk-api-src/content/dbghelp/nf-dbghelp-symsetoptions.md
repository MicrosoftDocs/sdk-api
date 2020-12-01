---
UID: NF:dbghelp.SymSetOptions
title: SymSetOptions function (dbghelp.h)
description: Sets the options mask.
helpviewer_keywords: ["SYMOPT_ALLOW_ABSOLUTE_SYMBOLS","SYMOPT_ALLOW_ZERO_ADDRESS","SYMOPT_AUTO_PUBLICS","SYMOPT_CASE_INSENSITIVE","SYMOPT_DEBUG","SYMOPT_DEFERRED_LOADS","SYMOPT_DISABLE_SYMSRV_AUTODETECT","SYMOPT_EXACT_SYMBOLS","SYMOPT_FAIL_CRITICAL_ERRORS","SYMOPT_FAVOR_COMPRESSED","SYMOPT_FLAT_DIRECTORY","SYMOPT_IGNORE_CVREC","SYMOPT_IGNORE_IMAGEDIR","SYMOPT_IGNORE_NT_SYMPATH","SYMOPT_INCLUDE_32BIT_MODULES","SYMOPT_LOAD_ANYTHING","SYMOPT_LOAD_LINES","SYMOPT_NO_CPP","SYMOPT_NO_IMAGE_SEARCH","SYMOPT_NO_PROMPTS","SYMOPT_NO_PUBLICS","SYMOPT_NO_UNQUALIFIED_LOADS","SYMOPT_OVERWRITE","SYMOPT_PUBLICS_ONLY","SYMOPT_SECURE","SYMOPT_UNDNAME","SymSetOptions","SymSetOptions function","_win32_symsetoptions","base.symsetoptions","dbghelp/SymSetOptions"]
old-location: base\symsetoptions.htm
tech.root: Debug
ms.assetid: 15d72415-829f-4ba3-af80-1f3762cbebda
ms.date: 12/05/2018
ms.keywords: SYMOPT_ALLOW_ABSOLUTE_SYMBOLS, SYMOPT_ALLOW_ZERO_ADDRESS, SYMOPT_AUTO_PUBLICS, SYMOPT_CASE_INSENSITIVE, SYMOPT_DEBUG, SYMOPT_DEFERRED_LOADS, SYMOPT_DISABLE_SYMSRV_AUTODETECT, SYMOPT_EXACT_SYMBOLS, SYMOPT_FAIL_CRITICAL_ERRORS, SYMOPT_FAVOR_COMPRESSED, SYMOPT_FLAT_DIRECTORY, SYMOPT_IGNORE_CVREC, SYMOPT_IGNORE_IMAGEDIR, SYMOPT_IGNORE_NT_SYMPATH, SYMOPT_INCLUDE_32BIT_MODULES, SYMOPT_LOAD_ANYTHING, SYMOPT_LOAD_LINES, SYMOPT_NO_CPP, SYMOPT_NO_IMAGE_SEARCH, SYMOPT_NO_PROMPTS, SYMOPT_NO_PUBLICS, SYMOPT_NO_UNQUALIFIED_LOADS, SYMOPT_OVERWRITE, SYMOPT_PUBLICS_ONLY, SYMOPT_SECURE, SYMOPT_UNDNAME, SymSetOptions, SymSetOptions function, _win32_symsetoptions, base.symsetoptions, dbghelp/SymSetOptions
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymSetOptions
 - dbghelp/SymSetOptions
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
 - SymSetOptions
---

# SymSetOptions function


## -description

Sets the options mask.

## -parameters

### -param SymOptions [in]

The symbol options. Zero is a valid value and indicates that all options are turned off. The options values are combined using the OR operator to form a valid options value. The following are valid values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_ALLOW_ABSOLUTE_SYMBOLS"></a><a id="symopt_allow_absolute_symbols"></a><dl>
<dt><b>SYMOPT_ALLOW_ABSOLUTE_SYMBOLS</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Enables the use of symbols that are stored with absolute addresses. Most symbols are stored as RVAs from the base of the module. DbgHelp translates them to absolute addresses. There are symbols that are stored as an absolute address. These have very specialized purposes and are typically not used.

<b>DbgHelp 5.1 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_ALLOW_ZERO_ADDRESS"></a><a id="symopt_allow_zero_address"></a><dl>
<dt><b>SYMOPT_ALLOW_ZERO_ADDRESS</b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Enables the use of symbols that do not have an address. By default, DbgHelp filters out symbols that do not have an address.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_AUTO_PUBLICS"></a><a id="symopt_auto_publics"></a><dl>
<dt><b>SYMOPT_AUTO_PUBLICS</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Do not search the public symbols when searching for symbols by address, or when enumerating symbols, unless they were not found in the global symbols or within the current scope. This option has no effect with <b>SYMOPT_PUBLICS_ONLY</b>.

<b>DbgHelp 5.1 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_CASE_INSENSITIVE"></a><a id="symopt_case_insensitive"></a><dl>
<dt><b>SYMOPT_CASE_INSENSITIVE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
All symbol searches are insensitive to case.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_DEBUG"></a><a id="symopt_debug"></a><dl>
<dt><b>SYMOPT_DEBUG</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Pass debug output through <a href="/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw">OutputDebugString</a> or the  <a href="/windows/desktop/api/dbghelp/nc-dbghelp-psymbol_registered_callback">SymRegisterCallbackProc64</a> callback function.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_DEFERRED_LOADS"></a><a id="symopt_deferred_loads"></a><dl>
<dt><b>SYMOPT_DEFERRED_LOADS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Symbols are not loaded until a reference is made requiring the symbols be loaded. This is the fastest, most efficient way to use the symbol handler.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_DISABLE_SYMSRV_AUTODETECT"></a><a id="symopt_disable_symsrv_autodetect"></a><dl>
<dt><b>SYMOPT_DISABLE_SYMSRV_AUTODETECT</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
Disables the auto-detection of symbol server stores in the symbol path, even without the "SRV*" designation, maintaining compatibility with previous behavior.

<b>DbgHelp 6.6 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_EXACT_SYMBOLS"></a><a id="symopt_exact_symbols"></a><dl>
<dt><b>SYMOPT_EXACT_SYMBOLS</b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Do not load an unmatched .pdb file. Do not load export symbols if all else fails.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_FAIL_CRITICAL_ERRORS"></a><a id="symopt_fail_critical_errors"></a><dl>
<dt><b>SYMOPT_FAIL_CRITICAL_ERRORS</b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Do not display system dialog boxes when there is a media failure such as no media in a drive. Instead, the failure happens silently.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_FAVOR_COMPRESSED"></a><a id="symopt_favor_compressed"></a><dl>
<dt><b>SYMOPT_FAVOR_COMPRESSED</b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
If there is both an uncompressed and a compressed file available, favor the compressed file. This option is good for slow connections.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_FLAT_DIRECTORY"></a><a id="symopt_flat_directory"></a><dl>
<dt><b>SYMOPT_FLAT_DIRECTORY</b></dt>
<dt>0x00400000</dt>
</dl>
</td>
<td width="60%">
Symbols are stored in the root directory of the default downstream store.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_IGNORE_CVREC"></a><a id="symopt_ignore_cvrec"></a><dl>
<dt><b>SYMOPT_IGNORE_CVREC</b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Ignore path information in the CodeView record of the image header when loading a .pdb file.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_IGNORE_IMAGEDIR"></a><a id="symopt_ignore_imagedir"></a><dl>
<dt><b>SYMOPT_IGNORE_IMAGEDIR</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Ignore the image directory.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_IGNORE_NT_SYMPATH"></a><a id="symopt_ignore_nt_sympath"></a><dl>
<dt><b>SYMOPT_IGNORE_NT_SYMPATH</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Do not use the path specified by <b>_NT_SYMBOL_PATH</b> if the user calls 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> without a valid path.

<b>DbgHelp 5.1:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_INCLUDE_32BIT_MODULES"></a><a id="symopt_include_32bit_modules"></a><dl>
<dt><b>SYMOPT_INCLUDE_32BIT_MODULES</b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
When debugging on 64-bit Windows, include any 32-bit modules.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_LOAD_ANYTHING"></a><a id="symopt_load_anything"></a><dl>
<dt><b>SYMOPT_LOAD_ANYTHING</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Disable checks to ensure a file (.exe, .dbg., or .pdb) is the correct file. Instead, load the first file located.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_LOAD_LINES"></a><a id="symopt_load_lines"></a><dl>
<dt><b>SYMOPT_LOAD_LINES</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Loads line number information.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_NO_CPP"></a><a id="symopt_no_cpp"></a><dl>
<dt><b>SYMOPT_NO_CPP</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
All C++ decorated symbols containing the symbol separator "::" are replaced by "__". This option exists for debuggers that cannot handle parsing real C++ symbol names.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_NO_IMAGE_SEARCH"></a><a id="symopt_no_image_search"></a><dl>
<dt><b>SYMOPT_NO_IMAGE_SEARCH</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Do not search the image for the symbol path when loading the symbols for a module if the module header cannot be read.

<b>DbgHelp 5.1:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_NO_PROMPTS"></a><a id="symopt_no_prompts"></a><dl>
<dt><b>SYMOPT_NO_PROMPTS</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Prevents prompting for validation from the symbol server.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_NO_PUBLICS"></a><a id="symopt_no_publics"></a><dl>
<dt><b>SYMOPT_NO_PUBLICS</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Do not search the publics table for symbols. This option should have little effect because there are copies of the public symbols in the globals table.

<b>DbgHelp 5.1:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_NO_UNQUALIFIED_LOADS"></a><a id="symopt_no_unqualified_loads"></a><dl>
<dt><b>SYMOPT_NO_UNQUALIFIED_LOADS</b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Prevents symbols from being loaded when the caller examines symbols across multiple modules. Examine only the module whose symbols have already been loaded.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_OVERWRITE"></a><a id="symopt_overwrite"></a><dl>
<dt><b>SYMOPT_OVERWRITE</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Overwrite the downlevel store from the symbol store.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_PUBLICS_ONLY"></a><a id="symopt_publics_only"></a><dl>
<dt><b>SYMOPT_PUBLICS_ONLY</b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Do not use private symbols. The version of DbgHelp that shipped with earlier Windows release supported only public symbols; this option provides compatibility with this limitation.

<b>DbgHelp 5.1:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_SECURE"></a><a id="symopt_secure"></a><dl>
<dt><b>SYMOPT_SECURE</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
DbgHelp will not load any symbol server other than SymSrv. SymSrv will not use the downstream store specified in <b>_NT_SYMBOL_PATH</b>. After this flag has been set, it cannot be cleared.

<b>DbgHelp 6.0 and 6.1:  </b>This flag can be cleared.

<b>DbgHelp 5.1:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMOPT_UNDNAME"></a><a id="symopt_undname"></a><dl>
<dt><b>SYMOPT_UNDNAME</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
All symbols are presented in undecorated form. 




This option has no effect on global or local symbols because they are stored undecorated. This option applies only to public symbols.

</td>
</tr>
</table>

## -returns

The function returns the current options mask.

## -remarks

The options value can be changed any number of times while the library is in use by an application. The option change affects all future calls to the symbol handler.

To get the current options mask, call the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetoptions">SymGetOptions</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.


#### Examples

For an example, see 
<a href="/windows/desktop/Debug/initializing-the-symbol-handler">Initializing the Symbol Handler</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetoptions">SymGetOptions</a>