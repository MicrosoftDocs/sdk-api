---
UID: NF:dbghelp.SymGetSourceVarFromTokenW
title: SymGetSourceVarFromTokenW function (dbghelp.h)
description: Retrieves the value associated with the specified variable name from the Source Server token.helpviewer_keywords: ["SymGetSourceVarFromToken","SymGetSourceVarFromToken function","SymGetSourceVarFromTokenW","base.symgetsourcevarfromtoken","dbghelp/SymGetSourceVarFromToken","dbghelp/SymGetSourceVarFromTokenW"]
old-location: base\symgetsourcevarfromtoken.htm
tech.root: Debug
ms.assetid: 05e9005a-aef3-44a3-a73b-21830799a3d5
ms.date: 12/05/2018
ms.keywords: SymGetSourceVarFromToken, SymGetSourceVarFromToken function, SymGetSourceVarFromTokenW, base.symgetsourcevarfromtoken, dbghelp/SymGetSourceVarFromToken, dbghelp/SymGetSourceVarFromTokenW
f1_keywords:
- dbghelp/SymGetSourceVarFromToken
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
req.unicode-ansi: SymGetSourceVarFromTokenW (Unicode) and SymGetSourceVarFromToken (ANSI)
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
- SymGetSourceVarFromToken
- SymGetSourceVarFromToken
- SymGetSourceVarFromTokenW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
---

# SymGetSourceVarFromTokenW function


## -description


Retrieves the value associated with the specified variable name from the <a href="https://docs.microsoft.com/windows/desktop/Debug/source-server-and-source-indexing">Source Server</a> token.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param Token [in]

A pointer to the token.


### -param Params [in, optional]

This parameter is unused.


### -param VarName [in]

The name of the variable token whose value you want to retrieve.


### -param Value [out]

A pointer to a 
buffer that receives the value associated with the variable token specified in the <i>VarName</i> parameter.


### -param Size [in]

The size of the <i>Value</i> buffer, in characters.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.



