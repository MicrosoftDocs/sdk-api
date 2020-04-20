---
UID: NF:dbghelp.SymGetSourceFileW
title: SymGetSourceFileW function (dbghelp.h)
description: Retrieves the specified source file from the source server.helpviewer_keywords: ["SymGetSourceFile","SymGetSourceFile function","SymGetSourceFileW","base.symgetsourcefile","dbghelp/SymGetSourceFile","dbghelp/SymGetSourceFileW"]
old-location: base\symgetsourcefile.htm
tech.root: Debug
ms.assetid: 1d2115fb-2725-4fae-abb7-ff1b8a802c69
ms.date: 12/05/2018
ms.keywords: SymGetSourceFile, SymGetSourceFile function, SymGetSourceFileW, base.symgetsourcefile, dbghelp/SymGetSourceFile, dbghelp/SymGetSourceFileW
f1_keywords:
- dbghelp/SymGetSourceFile
dev_langs:
- c++
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetSourceFileW (Unicode) and SymGetSourceFile (ANSI)
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
api_name:
- SymGetSourceFile
- SymGetSourceFile
- SymGetSourceFileW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# SymGetSourceFileW function


## -description


Retrieves the specified source file from the source server.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param Base [in]

The base address of the module. 


### -param Params [in, optional]

This parameter is unused.


### -param FileSpec [in]

The name of the source file.


### -param FilePath [out]

A pointer to a 
buffer that receives the fully qualified path of the source file.


### -param Size [in]

The size of the <i>FilePath</i> buffer, in characters.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To control which directory receives the source files, use the <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symsethomedirectory">SymSetHomeDirectory</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/source-server-and-source-indexing">Source Server</a>
 

 

