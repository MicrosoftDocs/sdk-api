---
UID: NF:dbghelp.SymUnDName
title: SymUnDName function (dbghelp.h)
description: Undecorates a decorated C++ symbol name. (SymUnDName)
helpviewer_keywords: ["SymUnDName","SymUnDName function","SymUnDName64","SymUnDName64 function","base.symundname64","dbghelp/SymUnDName","dbghelp/SymUnDName64"]
old-location: base\symundname64.htm
tech.root: Debug
ms.assetid: f7bea3a4-5e17-4743-894f-8eb8f9992cac
ms.date: 12/05/2018
ms.keywords: SymUnDName, SymUnDName function, SymUnDName64, SymUnDName64 function, base.symundname64, dbghelp/SymUnDName, dbghelp/SymUnDName64
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymUnDName
 - dbghelp/SymUnDName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - SymUnDName64
 - SymUnDName
---

# SymUnDName function


## -description

Undecorates a decorated C++ symbol name.

Applications can also use the <a href="/windows/desktop/api/dbghelp/nf-dbghelp-undecoratesymbolname">UnDecorateSymbolName</a> function.

## -parameters

### -param sym [in]

A pointer to an 
<a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_symbol">IMAGEHLP_SYMBOL64</a> structure that specifies the symbol to be undecorated.

### -param UnDecName [out]

A pointer to a buffer that receives the undecorated name.

### -param UnDecNameLength [in]

The size of the <i>UnDecName</i> buffer, in characters.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

This function supersedes the <b>SymUnDName</b> function. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>SymUnDName</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define SymUnDName SymUnDName64
#else
BOOL
IMAGEAPI
SymUnDName(
    __in PIMAGEHLP_SYMBOL sym,  
    __out_ecount(UnDecNameLength) PSTR UnDecName,   
    __in DWORD UnDecNameLength 
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-undecoratesymbolname">UnDecorateSymbolName</a>
