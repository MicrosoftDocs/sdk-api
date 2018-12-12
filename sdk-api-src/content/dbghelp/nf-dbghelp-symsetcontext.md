---
UID: NF:dbghelp.SymSetContext
title: SymSetContext function
author: windows-sdk-content
description: Sets context information used by the SymEnumSymbols function. This function only works with PDB symbols.
old-location: base\symsetcontext.htm
tech.root: Debug
ms.assetid: 0a9c6bfe-5e60-48c4-af98-b910df3032d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymSetContext, SymSetContext function, _win32_symsetcontext, base.symsetcontext, dbghelp/SymSetContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - SymSetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# SymSetContext function


## -description


Sets context information used by the 
    <a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a> function. This function only works with 
    PDB symbols.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param StackFrame [in]

A pointer to an <a href="https://msdn.microsoft.com/b6c89cf2-b108-4518-9f4c-4a3684b3f0a7">IMAGEHLP_STACK_FRAME</a> 
      structure that contains frame information.


### -param Context [in, optional]

This parameter is ignored.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If you call <b>SymSetContext</b> to set the context to its 
    current value, the function fails but <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> 
    returns <b>ERROR_SUCCESS</b>.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to 
    this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize 
    all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/b6c89cf2-b108-4518-9f4c-4a3684b3f0a7">IMAGEHLP_STACK_FRAME</a>



<a href="https://msdn.microsoft.com/e1232657-baf6-4e5b-9995-a382aa1391c2">SymEnumSymbols</a>
 

 

