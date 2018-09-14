---
UID: NF:dbghelp.SymGetSymbolFile
title: SymGetSymbolFile function
author: windows-sdk-content
description: Locates a symbol file in the specified symbol path.
old-location: base\symgetsymbolfile.htm
tech.root: Debug
ms.assetid: 8e78e0ef-e68c-4270-8c63-9513f3069ed0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SymGetSymbolFile, SymGetSymbolFile function, SymGetSymbolFileW, base.symgetsymbolfile, dbghelp/SymGetSymbolFile, dbghelp/SymGetSymbolFileW, sfDbg, sfImage, sfMpd, sfPdb
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
req.unicode-ansi: SymGetSymbolFileW (Unicode) and SymGetSymbolFile (ANSI)
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
 - SymGetSymbolFile
 - SymGetSymbolFile
 - SymGetSymbolFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.3 or later
---

# SymGetSymbolFile function


## -description


Locates a symbol file in the specified symbol path.


## -parameters




### -param hProcess [in, optional]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function. 

If this handle is 0, <i>SymPath</i> cannot be <b>NULL</b>. Use this option to load a symbol file without calling <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> or <a href="https://msdn.microsoft.com/56107b71-a3f9-49af-9a90-df3585aed7c8">SymCleanup</a>.


### -param SymPath [in, optional]

The symbol path. If this parameter is <b>NULL</b> or an empty string, the function uses the symbol path set using the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> or <a href="https://msdn.microsoft.com/564ba1f6-65c6-4c45-bdbf-41ef0dd8a39d">SymSetSearchPath</a> function.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns a value that indicates why the symbol file was not returned.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

