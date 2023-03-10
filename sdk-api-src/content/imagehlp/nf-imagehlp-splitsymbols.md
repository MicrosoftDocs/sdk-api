---
UID: NF:imagehlp.SplitSymbols
title: SplitSymbols function (imagehlp.h)
description: Strips symbols from the specified image.
helpviewer_keywords: ["SPLITSYM_EXTRACT_ALL","SPLITSYM_REMOVE_PRIVATE","SPLITSYM_SYMBOLPATH_IS_SRC","SplitSymbols","SplitSymbols function","_win32_splitsymbols","base.splitsymbols","imagehlp/SplitSymbols"]
old-location: base\splitsymbols.htm
tech.root: Debug
ms.assetid: b9b940ce-8349-472e-b802-b477bd195b63
ms.date: 12/05/2018
ms.keywords: SPLITSYM_EXTRACT_ALL, SPLITSYM_REMOVE_PRIVATE, SPLITSYM_SYMBOLPATH_IS_SRC, SplitSymbols, SplitSymbols function, _win32_splitsymbols, base.splitsymbols, imagehlp/SplitSymbols
req.header: imagehlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Imagehlp.lib
req.dll: Imagehlp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SplitSymbols
 - imagehlp/SplitSymbols
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Imagehlp.dll
api_name:
 - SplitSymbols
---

# SplitSymbols function


## -description

Strips symbols from the specified image.

## -parameters

### -param ImageName [in]

The name of the image from which to split symbols.

### -param SymbolsPath [in]

The subdirectory for storing symbols. This parameter is optional.

### -param SymbolFilePath [out]

The name of the generated symbol file. This file typically has a .dbg extension.

### -param Flags [in]

The information to be split from the image. This parameter can be zero or a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SPLITSYM_EXTRACT_ALL"></a><a id="splitsym_extract_all"></a><dl>
<dt><b>SPLITSYM_EXTRACT_ALL</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Usually, an image with the symbols split off will still contain a MISC debug directory with the name of the symbol file. Therefore, the debugger can still find the symbols. Using this flag removes this link. The end result is similar to using the <b>-debug:none</b> switch on the Microsoft linker.

</td>
</tr>
<tr>
<td width="40%"><a id="SPLITSYM_REMOVE_PRIVATE"></a><a id="splitsym_remove_private"></a><dl>
<dt><b>SPLITSYM_REMOVE_PRIVATE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
This strips off the private CodeView symbolic information when generating the symbol file.

</td>
</tr>
<tr>
<td width="40%"><a id="SPLITSYM_SYMBOLPATH_IS_SRC"></a><a id="splitsym_symbolpath_is_src"></a><dl>
<dt><b>SPLITSYM_SYMBOLPATH_IS_SRC</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The symbol file path contains an alternate path to locate the .pdb file.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SplitSymbols</b> function should be used when stripping symbols from an image. It will create a symbol file that all compatible debuggers understand. The format is defined in WinNT.h and consists of an image header, followed by the array of section headers, the FPO information, and all debugging symbolic information from the image.

If the <i>SymbolsPath</i> parameter is <b>NULL</b>, the symbol file is stored in the directory where the image exists. Otherwise, it is stored in the subdirectory below <i>SymbolsPath</i> that matches the extension of the image. Using this method reduces the chances of symbol file collision. For example, the symbols for myapp.exe will be in the <i>SymbolsPath</i>\exe directory and the symbols for myapp.dll will be in the <i>SymbolsPath</i>\dll directory.

All ImageHlp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

## -see-also

<a href="/windows/desktop/Debug/imagehlp-functions">ImageHlp Functions</a>