---
UID: NC:dbghelp.PSYM_ENUMSOURCEFILES_CALLBACKW
title: PSYM_ENUMSOURCEFILES_CALLBACKW (dbghelp.h)
description: An application-defined callback function used with the SymEnumSourceFiles function.
helpviewer_keywords: ["PSYM_ENUMSOURCEFILES_CALLBACK","PSYM_ENUMSOURCEFILES_CALLBACKW","SymEnumSourceFilesProc","SymEnumSourceFilesProc callback","SymEnumSourceFilesProc callback function","base.symenumsourcefilesproc","dbghelp/SymEnumSourceFilesProc"]
old-location: base\symenumsourcefilesproc.htm
tech.root: Debug
ms.assetid: b1d1e967-514d-43da-b470-23228fa03dd9
ms.date: 12/05/2018
ms.keywords: PSYM_ENUMSOURCEFILES_CALLBACK, PSYM_ENUMSOURCEFILES_CALLBACKW, SymEnumSourceFilesProc, SymEnumSourceFilesProc callback, SymEnumSourceFilesProc callback function, base.symenumsourcefilesproc, dbghelp/SymEnumSourceFilesProc
f1_keywords:
- dbghelp/SymEnumSourceFilesProc
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
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- DbgHelp.h
api_name:
- SymEnumSourceFilesProc
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# PSYM_ENUMSOURCEFILES_CALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a> function.

The <b>PSYM_ENUMSOURCEFILES_CALLBACK</b> and <b>PSYM_ENUMSOURCEFILES_CALLBACKW</b> types define a pointer to this callback function. 
<b>SymEnumSourceFilesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param pSourceFile [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-sourcefile">SOURCEFILE</a> structure that provides information about the source file.


### -param UserContext [in, optional]

The user-defined value passed from the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns



If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-sourcefile">SOURCEFILE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcefiles">SymEnumSourceFiles</a>
 

 

