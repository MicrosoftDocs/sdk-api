---
UID: NF:dbghelp.SymPrevW
title: SymPrevW function (dbghelp.h)
description: Retrieves symbol information for the previous symbol.
old-location: base\symprev.htm
tech.root: Debug
ms.assetid: 45503f0c-cb66-4ddf-986d-02de7fc480f2
ms.date: 12/05/2018
ms.keywords: SymPrev, SymPrev function, SymPrevW, base.symprev, dbghelp/SymPrev, dbghelp/SymPrevW
ms.topic: function
f1_keywords:
- dbghelp/SymPrev
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
req.unicode-ansi: SymPrevW (Unicode) and SymPrev (ANSI)
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
- SymPrev
- SymPrev
- SymPrevW
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
---

# SymPrevW function


## -description


Retrieves symbol information for the previous symbol.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.


### -param siw

TBD




#### - si [in, out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure that provides information about the current symbol. Upon return, the structure contains information about the previous symbol.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



This function requires that the <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a> structure have valid data for the current symbol. The previous symbol is the symbol with a virtual address that immediately precedes this symbol.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-symbol_info">SYMBOL_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symnext">SymNext</a>
 

 

