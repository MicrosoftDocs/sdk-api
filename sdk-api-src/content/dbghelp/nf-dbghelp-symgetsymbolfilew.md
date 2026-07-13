---
UID: NF:dbghelp.SymGetSymbolFileW
title: SymGetSymbolFileW function (dbghelp.h)
description: The SymGetSymbolFileW (Unicode) function locates a symbol file in the specified symbol path.
helpviewer_keywords: ["SymGetSymbolFile","SymGetSymbolFile function","SymGetSymbolFileW","base.symgetsymbolfile","dbghelp/SymGetSymbolFile","dbghelp/SymGetSymbolFileW","sfDbg","sfImage","sfMpd","sfPdb"]
old-location: base\symgetsymbolfile.htm
tech.root: Debug
ms.assetid: 8e78e0ef-e68c-4270-8c63-9513f3069ed0
ms.date: 08/04/2022
ms.keywords: SymGetSymbolFile, SymGetSymbolFile function, SymGetSymbolFileW, base.symgetsymbolfile, dbghelp/SymGetSymbolFile, dbghelp/SymGetSymbolFileW, sfDbg, sfImage, sfMpd, sfPdb
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetSymbolFileW (Unicode) and SymGetSymbolFile (ANSI)
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
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - SymGetSymbolFileW
 - dbghelp/SymGetSymbolFileW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
 - imagehlp.dll
api_name:
 - SymGetSymbolFile
 - SymGetSymbolFile
 - SymGetSymbolFileW
---

# SymGetSymbolFileW function


## -description

Locates a symbol file in the specified symbol path.

## -parameters

### -param hProcess [in, optional]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function. 

If this handle is 0, <i>SymPath</i> cannot be <b>NULL</b>. Use this option to load a symbol file without calling <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> or <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symcleanup">SymCleanup</a>.

### -param SymPath [in, optional]

The symbol path. If this parameter is <b>NULL</b> or an empty string, the function uses the symbol path set using the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> or <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.

### -param ImageFile [in]

The name of the image  file.

### -param Type [in]

The type of symbol file. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="sfImage"></a><a id="sfimage"></a><a id="SFIMAGE"></a><dl>
<dt><b>sfImage</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
A .exe or .dll file.

</td>
</tr>
<tr>
<td width="40%"><a id="sfDbg"></a><a id="sfdbg"></a><a id="SFDBG"></a><dl>
<dt><b>sfDbg</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A .dbg file.

</td>
</tr>
<tr>
<td width="40%"><a id="sfPdb"></a><a id="sfpdb"></a><a id="SFPDB"></a><dl>
<dt><b>sfPdb</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A .pdb file.

</td>
</tr>
<tr>
<td width="40%"><a id="sfMpd"></a><a id="sfmpd"></a><a id="SFMPD"></a><dl>
<dt><b>sfMpd</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Reserved.

</td>
</tr>
</table>

### -param SymbolFile [out]

A pointer to a null-terminated string that receives the name of the symbol file.

### -param cSymbolFile [in]

The size of the <i>SymbolFile</i> buffer, in characters.

### -param DbgFile [out]

A pointer to a buffer that receives the fully qualified path to the symbol file. This buffer must be at least MAX_PATH characters.

### -param cDbgFile [in]

The size of the <i>DbgFile</i> buffer, in characters.

## -returns

If the server locates a valid symbol file, it returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b> and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns a value that indicates why the symbol file was not returned.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymGetSymbolFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>
