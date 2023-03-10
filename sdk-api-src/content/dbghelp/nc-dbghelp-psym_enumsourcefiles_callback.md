---
UID: NC:dbghelp.PSYM_ENUMSOURCEFILES_CALLBACK
title: PSYM_ENUMSOURCEFILES_CALLBACK (dbghelp.h)
description: PSYM_ENUMSOURCEFILES_CALLBACK (dbghelp.h) is an application-defined callback function used with the SymEnumSourceFiles function.
helpviewer_keywords: ["PSYM_ENUMSOURCEFILES_CALLBACK","PSYM_ENUMSOURCEFILES_CALLBACKW","SymEnumSourceFilesProc","SymEnumSourceFilesProc callback","SymEnumSourceFilesProc callback function","base.symenumsourcefilesproc","dbghelp/SymEnumSourceFilesProc"]
old-location: base\symenumsourcefilesproc.htm
tech.root: Debug
ms.assetid: b1d1e967-514d-43da-b470-23228fa03dd9
ms.date: 08/03/2022
ms.keywords: PSYM_ENUMSOURCEFILES_CALLBACK, PSYM_ENUMSOURCEFILES_CALLBACKW, SymEnumSourceFilesProc, SymEnumSourceFilesProc callback, SymEnumSourceFilesProc callback function, base.symenumsourcefilesproc, dbghelp/SymEnumSourceFilesProc
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
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - PSYM_ENUMSOURCEFILES_CALLBACK
 - dbghelp/PSYM_ENUMSOURCEFILES_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymEnumSourceFilesProc
---

# PSYM_ENUMSOURCEFILES_CALLBACK callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a> function.

The <b>PSYM_ENUMSOURCEFILES_CALLBACK</b> and <b>PSYM_ENUMSOURCEFILES_CALLBACKW</b> types define a pointer to this callback function. 
<b>SymEnumSourceFilesProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param pSourceFile [in]

A pointer to a 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-sourcefile">SOURCEFILE</a> structure that provides information about the source file.

### -param UserContext [in, optional]

The user-defined value passed from the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.

## -returns

If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-sourcefile">SOURCEFILE</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a>
