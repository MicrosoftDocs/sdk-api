---
UID: NF:dbghelp.SymFunctionTableAccess64AccessRoutines
title: SymFunctionTableAccess64AccessRoutines function
author: windows-sdk-content
description: Finds a function table entry or frame pointer omission (FPO) record for an address.
old-location: base\symfunctiontableaccess64accessroutines.htm
old-project: Debug
ms.assetid: 7AE8779A-F3F8-45FF-B11C-4D48CF76FDCA
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SymFunctionTableAccess64AccessRoutines, SymFunctionTableAccess64AccessRoutines function, base.symfunctiontableaccess64accessroutines, dbghelp/SymFunctionTableAccess64AccessRoutines
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	DbgHelp.dll
api_name:
-	SymFunctionTableAccess64AccessRoutines
product: Windows
targetos: Windows
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
---

# SymFunctionTableAccess64AccessRoutines function


## -description


 Finds a function table entry or  frame pointer omission (FPO) record for an address.

Use <a href="https://msdn.microsoft.com/f79e6af9-9931-4bd7-ae12-29d890267a89">SymFunctionTableAccess64</a> instead.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param AddrBase [in]

The base address for which function table information is required.


### -param ReadMemoryRoutine [in, optional]

Pointer to a read memory callback function.


### -param GetModuleBaseRoutine [in, optional]

Pointer to a get module base callback function.


## -see-also




<a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a>
 

 

