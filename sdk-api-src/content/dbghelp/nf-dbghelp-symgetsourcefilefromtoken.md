---
UID: NF:dbghelp.SymGetSourceFileFromToken
title: SymGetSourceFileFromToken function (dbghelp.h)
description: Retrieves the source file associated with the specified token from the source server.
helpviewer_keywords: ["SymGetSourceFileFromToken","SymGetSourceFileFromToken function","SymGetSourceFileFromTokenW","base.symgetsourcefilefromtoken","dbghelp/SymGetSourceFileFromToken","dbghelp/SymGetSourceFileFromTokenW"]
old-location: base\symgetsourcefilefromtoken.htm
tech.root: Debug
ms.assetid: 67a282c2-99f8-4e35-9323-a81327404d1a
ms.date: 12/05/2018
ms.keywords: SymGetSourceFileFromToken, SymGetSourceFileFromToken function, SymGetSourceFileFromTokenW, base.symgetsourcefilefromtoken, dbghelp/SymGetSourceFileFromToken, dbghelp/SymGetSourceFileFromTokenW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetSourceFileFromTokenW (Unicode) and SymGetSourceFileFromToken (ANSI)
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
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - SymGetSourceFileFromToken
 - dbghelp/SymGetSourceFileFromToken
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
 - SymGetSourceFileFromToken
 - SymGetSourceFileFromToken
 - SymGetSourceFileFromTokenW
---

# SymGetSourceFileFromToken function


## -description

Retrieves the source file associated with the specified token from the source server.

## -parameters

### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param Token [in]

A pointer to the token.

### -param Params [in, optional]

This parameter is unused.

### -param FilePath [out]

A pointer to a 
buffer that receives the fully qualified path of the source file.

### -param Size [in]

The size of the <i>FilePath</i> buffer, in characters.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/Debug/source-server-and-source-indexing">Source Server</a>