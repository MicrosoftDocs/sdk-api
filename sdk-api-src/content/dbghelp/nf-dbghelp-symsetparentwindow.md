---
UID: NF:dbghelp.SymSetParentWindow
title: SymSetParentWindow function (dbghelp.h)
description: Sets the window that the caller will use to display a user interface.helpviewer_keywords: ["SymSetParentWindow","SymSetParentWindow function","_win32_symsetparentwindow","base.symsetparentwindow","dbghelp/SymSetParentWindow"]
old-location: base\symsetparentwindow.htm
tech.root: Debug
ms.assetid: 6c4532cd-695c-45a0-b8ea-3aed47308db1
ms.date: 12/05/2018
ms.keywords: SymSetParentWindow, SymSetParentWindow function, _win32_symsetparentwindow, base.symsetparentwindow, dbghelp/SymSetParentWindow
f1_keywords:
- dbghelp/SymSetParentWindow
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>
 

 

