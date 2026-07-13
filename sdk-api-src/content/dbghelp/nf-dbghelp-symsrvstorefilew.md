---
UID: NF:dbghelp.SymSrvStoreFileW
title: SymSrvStoreFileW function (dbghelp.h)
description: The SymSrvStoreFileW (Unicode) function (dbghelp.h) stores a file in the specified symbol store.
helpviewer_keywords: ["SYMSTOREOPT_COMPRESS","SYMSTOREOPT_OVERWRITE","SYMSTOREOPT_PASS_IF_EXISTS","SYMSTOREOPT_POINTER","SYMSTOREOPT_RETURNINDEX","SymSrvStoreFile","SymSrvStoreFile function","SymSrvStoreFileW","base.symsrvstorefile","dbghelp/SymSrvStoreFile","dbghelp/SymSrvStoreFileW"]
old-location: base\symsrvstorefile.htm
tech.root: Debug
ms.assetid: 308ce0bb-d5ff-4de0-b5b3-9e26aa7b163a
ms.date: 08/04/2022
ms.keywords: SYMSTOREOPT_COMPRESS, SYMSTOREOPT_OVERWRITE, SYMSTOREOPT_PASS_IF_EXISTS, SYMSTOREOPT_POINTER, SYMSTOREOPT_RETURNINDEX, SymSrvStoreFile, SymSrvStoreFile function, SymSrvStoreFileW, base.symsrvstorefile, dbghelp/SymSrvStoreFile, dbghelp/SymSrvStoreFileW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymSrvStoreFileW (Unicode) and SymSrvStoreFile (ANSI)
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
 - SymSrvStoreFileW
 - dbghelp/SymSrvStoreFileW
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
 - SymSrvStoreFile
 - SymSrvStoreFile
 - SymSrvStoreFileW
---

# SymSrvStoreFileW function


## -description

Stores a file in the specified symbol store.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param SrvPath [in, optional]

The symbol store.

### -param File [in]

The name of the file.

### -param Flags [in]

The flags that control the function. 
This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_COMPRESS"></a><a id="symstoreopt_compress"></a><dl>
<dt><b>SYMSTOREOPT_COMPRESS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Compress the file.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_OVERWRITE"></a><a id="symstoreopt_overwrite"></a><dl>
<dt><b>SYMSTOREOPT_OVERWRITE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Overwrite the file if it exists.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_PASS_IF_EXISTS"></a><a id="symstoreopt_pass_if_exists"></a><dl>
<dt><b>SYMSTOREOPT_PASS_IF_EXISTS</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Do not report an error if the file already exists in the symbol store.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_POINTER"></a><a id="symstoreopt_pointer"></a><dl>
<dt><b>SYMSTOREOPT_POINTER</b></dt>
<dt>0x08</dt>
</dl>
</td>
<td width="60%">
Store in File.ptr.

</td>
</tr>
<tr>
<td width="40%"><a id="SYMSTOREOPT_RETURNINDEX"></a><a id="symstoreopt_returnindex"></a><dl>
<dt><b>SYMSTOREOPT_RETURNINDEX</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Return the index only.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a pointer to a null-terminated string that specifies the full-qualified path to the stored file.
						

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy the data returned to another buffer immediately.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymSrvStoreFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
