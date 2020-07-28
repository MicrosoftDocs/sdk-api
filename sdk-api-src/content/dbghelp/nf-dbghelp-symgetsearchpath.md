---
UID: NF:dbghelp.SymGetSearchPath
title: SymGetSearchPath function (dbghelp.h)
description: Retrieves the symbol search path for the specified process.
helpviewer_keywords: ["SymGetSearchPath","SymGetSearchPath function","SymGetSearchPathW","_win32_symgetsearchpath","base.symgetsearchpath","dbghelp/SymGetSearchPath","dbghelp/SymGetSearchPathW"]
old-location: base\symgetsearchpath.htm
tech.root: Debug
ms.assetid: aa8c8450-ee67-4614-98a1-5feebdd3a788
ms.date: 12/05/2018
ms.keywords: SymGetSearchPath, SymGetSearchPath function, SymGetSearchPathW, _win32_symgetsearchpath, base.symgetsearchpath, dbghelp/SymGetSearchPath, dbghelp/SymGetSearchPathW
f1_keywords:
- dbghelp/SymGetSearchPath
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
req.unicode-ansi: SymGetSearchPathW (Unicode) and SymGetSearchPath (ANSI)
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
- SymGetSearchPath
- SymGetSearchPath
- SymGetSearchPathW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# SymGetSearchPath function


## -description


Retrieves the symbol search path for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param SearchPath [out]

A pointer to the buffer that receives the symbol search path.


### -param SearchPathLength [in]

The size of the <i>SearchPath</i> buffer, in characters.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The 
<b>SymGetSearchPath</b> function copies the symbol search path for the specified process into the <i>SearchPath</i> buffer. If the function fails, the contents of the buffer are undefined.

To specify a symbol search path for the process, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a>
 

 

