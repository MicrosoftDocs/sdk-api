---
UID: NF:dbghelp.SymAddSourceStreamA
tech.root: Debug 
title: SymAddSourceStreamA
ms.date: 04/14/2021
targetos: Windows
description: Adds the stream to the specified module for use by the Source Server. (SymAddSourceStreamA)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Dbghelp.dll 
req.header: dbghelp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Dbghelp.lib 
req.max-support: 
req.namespace: 
req.redist: DbgHelp.dll 6.8 or later 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymAddSourceStreamA
 - SymAddSourceStream
f1_keywords:
 - SymAddSourceStreamA
 - dbghelp/SymAddSourceStreamA
 - SymAddSourceStream
 - dbghelp/SymAddSourceStream
dev_langs:
 - c++
---

# SymAddSourceStreamA function

## -description

Adds the stream to the specified module for use by the <a href="/windows/desktop/Debug/source-server-and-source-indexing">Source Server</a>.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Base [in]

The base address of the module.

### -param StreamFile [in, optional]

A null-terminated string that contains the absolute or relative path to a file that contains the source indexing stream. Can be <b>NULL</b> if <i>Buffer</i> is not <b>NULL</b>.

### -param Buffer [in, optional]

A buffer that contains the source indexing stream. Can be <b>NULL</b> if <i>StreamFile</i> is not <b>NULL</b>.

### -param Size [in]

Size, in bytes, of the <i>Buffer</i> buffer.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SymAddSourceStream</b> adds a stream of data formatted for use by the <a href="/windows/desktop/Debug/source-server-and-source-indexing">source Server</a> to a designated module. The caller can pass the stream either as a buffer in the <i>Buffer</i> parameter or a file in the <i>StreamFile</i> parameter. If both parameters are filled, then the function uses the <i>Buffer</i> parameter. If both parameters are <b>NULL</b>, then the function returns <b>FALSE</b> and the <a href="/windows/desktop/Debug/last-error-code">last-error code</a> is set to <b>ERROR_INVALID_PARAMETER</b>.

It is important to note that <b>SymAddSourceStream</b> does not add the stream to any corresponding PDB in order to persist the data. This function is used by those programmatically implementing their own debuggers in scenarios in which a PDB is not available.

> [!NOTE]
> The dbghelp.h header defines SymAddSourceStream as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
