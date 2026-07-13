---
UID: NF:dbghelp.SymGetHomeDirectoryW
title: SymGetHomeDirectoryW function (dbghelp.h)
description: The SymGetHomeDirectoryW (Unicode) function retrieves the home directory used by Dbghelp.
helpviewer_keywords: ["SymGetHomeDirectory","SymGetHomeDirectory function","SymGetHomeDirectoryW","base.symgethomedirectory","dbghelp/SymGetHomeDirectory","dbghelp/SymGetHomeDirectoryW","hdBase","hdSrc","hdSym"]
old-location: base\symgethomedirectory.htm
tech.root: Debug
ms.assetid: 490de8cd-2738-4770-b708-fa2d61b83587
ms.date: 08/04/2022
ms.keywords: SymGetHomeDirectory, SymGetHomeDirectory function, SymGetHomeDirectoryW, base.symgethomedirectory, dbghelp/SymGetHomeDirectory, dbghelp/SymGetHomeDirectoryW, hdBase, hdSrc, hdSym
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetHomeDirectoryW (Unicode) and SymGetHomeDirectory (ANSI)
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
req.redist: DbgHelp.dll 6.1 or later
ms.custom: 19H1
f1_keywords:
 - SymGetHomeDirectoryW
 - dbghelp/SymGetHomeDirectoryW
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
 - SymGetHomeDirectory
 - SymGetHomeDirectory
 - SymGetHomeDirectoryW
---

# SymGetHomeDirectoryW function


## -description

Retrieves the home directory used by Dbghelp.

## -parameters

### -param type [in]

The directory to be retrieved. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="hdBase"></a><a id="hdbase"></a><a id="HDBASE"></a><dl>
<dt><b>hdBase</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The home directory.

</td>
</tr>
<tr>
<td width="40%"><a id="hdSrc"></a><a id="hdsrc"></a><a id="HDSRC"></a><dl>
<dt><b>hdSrc</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The source directory.

</td>
</tr>
<tr>
<td width="40%"><a id="hdSym"></a><a id="hdsym"></a><a id="HDSYM"></a><dl>
<dt><b>hdSym</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The symbol directory.

</td>
</tr>
</table>

### -param dir [out]

A pointer to a string that receives the directory.

### -param size [in]

The size of the output buffer, in characters.

## -returns

If the function succeeds, the return value is a pointer to the <i>dir</i> parameter.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymGetHomeDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsethomedirectory">SymSetHomeDirectory</a>
