---
UID: NF:dbghelp.SymSetParentWindow
title: SymSetParentWindow function
author: windows-sdk-content
description: Sets the window that the caller will use to display a user interface.
old-location: base\symsetparentwindow.htm
tech.root: Debug
ms.assetid: 6c4532cd-695c-45a0-b8ea-3aed47308db1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymSetParentWindow, SymSetParentWindow function, _win32_symsetparentwindow, base.symsetparentwindow, dbghelp/SymSetParentWindow
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
 - SymSetParentWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.0 or later
---

# SymSetParentWindow function


## -description


Sets the window that the caller will use to display a user interface.


## -parameters




### -param hwnd [in]

A handle to the window.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>
 

 

