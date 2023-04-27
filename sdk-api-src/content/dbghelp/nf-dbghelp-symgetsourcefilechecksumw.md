---
UID: NF:dbghelp.SymGetSourceFileChecksumW
title: SymGetSourceFileChecksumW function (dbghelp.h)
description: The SymGetSourceFileChecksumW (Unicode) function retrieves the specified source file checksum from the source server.
helpviewer_keywords: ["SymGetSourceFileChecksum","SymGetSourceFileChecksum function","SymGetSourceFileChecksumW","base.symgetsourcefilechecksum","dbghelp/SymGetSourceFileChecksum","dbghelp/SymGetSourceFileChecksumW"]
old-location: base\symgetsourcefilechecksum.htm
tech.root: Debug
ms.assetid: 6F45FEC4-AFB9-4612-A840-B806034F33E2
ms.date: 08/04/2022
ms.keywords: SymGetSourceFileChecksum, SymGetSourceFileChecksum function, SymGetSourceFileChecksumW, base.symgetsourcefilechecksum, dbghelp/SymGetSourceFileChecksum, dbghelp/SymGetSourceFileChecksumW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetSourceFileChecksumW (Unicode) and SymGetSourceFileChecksum (ANSI)
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
req.redist: DbgHelp.dll 10.0.15063 or later
ms.custom: 19H1
f1_keywords:
 - SymGetSourceFileChecksumW
 - dbghelp/SymGetSourceFileChecksumW
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
 - SymGetSourceFileChecksum
 - SymGetSourceFileChecksum
 - SymGetSourceFileChecksumW
---

# SymGetSourceFileChecksumW function


## -description

Retrieves the specified source file checksum from the source server.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Base [in]

The base address of the module.

### -param FileSpec [in]

The name of the source file.

### -param pCheckSumType [out]

On success, points to the checksum type.

### -param pChecksum [out]

pointer to a buffer that receives the checksum. If <b>NULL</b>, then when the call returns <i>pActualBytesWritten</i> returns the number of bytes required.

### -param checksumSize [in]

The size of the <i>pChecksum</i> buffer, in bytes.

### -param pActualBytesWritten [out]

Pointer to the actual bytes written in the buffer.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.
