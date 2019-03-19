---
UID: NC:dbghelp.PSYM_ENUMSOURCEFILES_CALLBACKW
title: PSYM_ENUMSOURCEFILES_CALLBACKW (dbghelp.h)
author: windows-sdk-content
description: An application-defined callback function used with the SymEnumSourceFiles function.
old-location: base\symenumsourcefilesproc.htm
tech.root: Debug
ms.assetid: b1d1e967-514d-43da-b470-23228fa03dd9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PSYM_ENUMSOURCEFILES_CALLBACK, PSYM_ENUMSOURCEFILES_CALLBACKW, SymEnumSourceFilesProc, SymEnumSourceFilesProc callback, SymEnumSourceFilesProc callback function, base.symenumsourcefilesproc, dbghelp/SymEnumSourceFilesProc
ms.topic: callback
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
---

# PSYM_ENUMSOURCEFILES_CALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/4649bdc6-74c5-4529-bedc-64e0277144d0">SymEnumSourceFiles</a> function.

The <b>PSYM_ENUMSOURCEFILES_CALLBACK</b> and <b>PSYM_ENUMSOURCEFILES_CALLBACKW</b> types define a pointer to this callback function. 
<b>SymEnumSourceFilesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param pSourceFile [in]

A pointer to a 
<a href="https://msdn.microsoft.com/b41b844d-85d2-4ea3-bdd9-1564898da9e1">SOURCEFILE</a> structure that provides information about the source file.


### -param UserContext [in, optional]

The user-defined value passed from the 
<a href="https://msdn.microsoft.com/4649bdc6-74c5-4529-bedc-64e0277144d0">SymEnumSourceFiles</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns



If the function returns <b>TRUE</b>, the enumeration will continue.
						

If the function returns <b>FALSE</b>, the enumeration will stop.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/b41b844d-85d2-4ea3-bdd9-1564898da9e1">SOURCEFILE</a>



<a href="https://msdn.microsoft.com/4649bdc6-74c5-4529-bedc-64e0277144d0">SymEnumSourceFiles</a>
 

 

