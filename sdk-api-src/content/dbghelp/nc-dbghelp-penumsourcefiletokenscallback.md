---
UID: NC:dbghelp.PENUMSOURCEFILETOKENSCALLBACK
title: PENUMSOURCEFILETOKENSCALLBACK (dbghelp.h)
description: An application-defined callback function used with the SymEnumSourceFileTokens function which enumerates the source server version control information stored in the PDB for a module.
helpviewer_keywords: ["PENUMSOURCEFILETOKENSCALLBACK","PENUMSOURCEFILETOKENSCALLBACK callback","SymEnumSourceFileTokensProc","SymEnumSourceFileTokensProc callback function","base.symenumsourcefiletokensproc","dbghelp/SymEnumSourceFileTokensProc"]
old-location: base\symenumsourcefiletokensproc.htm
tech.root: Debug
ms.assetid: 20c0eb1e-671b-4d31-88d4-57f2c149fcd9
ms.date: 12/05/2018
ms.keywords: PENUMSOURCEFILETOKENSCALLBACK, PENUMSOURCEFILETOKENSCALLBACK callback, SymEnumSourceFileTokensProc, SymEnumSourceFileTokensProc callback function, base.symenumsourcefiletokensproc, dbghelp/SymEnumSourceFileTokensProc
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.8 or later
ms.custom: 19H1
f1_keywords:
 - PENUMSOURCEFILETOKENSCALLBACK
 - dbghelp/PENUMSOURCEFILETOKENSCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dbghelp.h
api_name:
 - SymEnumSourceFileTokensProc
---

# PENUMSOURCEFILETOKENSCALLBACK callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiletokens">SymEnumSourceFileTokens</a> function which enumerates the <a href="/windows/desktop/Debug/source-server-and-source-indexing">source server</a> version control information stored in the PDB for a module.

The <b>PENUMSOURCEFILETOKENSCALLBACK</b> type defines a pointer to this callback function. 
<b>SymEnumSourceFileTokensProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param token [in]

A pointer to an opaque data structure that contains the version control information corresponding to a particular individual source file.     The usage of this token is detailed below.

### -param size [in]

The size of the data in the <i>token</i> parameter.

## -returns

If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.

## -remarks

An application can use this token to extract a source file from version control by calling <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsourcefilefromtoken">SymGetSourceFileFromToken</a>.  

To get individual variables from the token, call <a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsourcevarfromtoken">SymGetSourceVarFromToken</a>.  The names of the variables differ based on the scripts used to create the tokens.  See <a href="/windows/desktop/Debug/source-server-and-source-indexing">Source Server</a> for details.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/Debug/source-server-and-source-indexing">Source Server</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiletokens">SymEnumSourceFileTokens</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsourcefile">SymGetSourceFile</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgetsourcefilefromtoken">SymGetSourceFileFromToken</a>