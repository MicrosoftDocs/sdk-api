---
UID: NF:dbghelp.SymGetSearchPathW
title: SymGetSearchPathW function (dbghelp.h)
description: The SymGetSearchPathW (Unicode) function retrieves the symbol search path for the specified process.
helpviewer_keywords: ["SymGetSearchPath","SymGetSearchPath function","SymGetSearchPathW","_win32_symgetsearchpath","base.symgetsearchpath","dbghelp/SymGetSearchPath","dbghelp/SymGetSearchPathW"]
old-location: base\symgetsearchpath.htm
tech.root: Debug
ms.assetid: aa8c8450-ee67-4614-98a1-5feebdd3a788
ms.date: 08/04/2022
ms.keywords: SymGetSearchPath, SymGetSearchPath function, SymGetSearchPathW, _win32_symgetsearchpath, base.symgetsearchpath, dbghelp/SymGetSearchPath, dbghelp/SymGetSearchPathW
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - SymGetSearchPathW
 - dbghelp/SymGetSearchPathW
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
 - SymGetSearchPath
 - SymGetSearchPath
 - SymGetSearchPathW
---

# SymGetSearchPathW function


## -description

Retrieves the symbol search path for the specified process.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param SearchPath [out]

A pointer to the buffer that receives the symbol search path.

### -param SearchPathLength [in]

The size of the <i>SearchPath</i> buffer, in characters.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>SymGetSearchPath</b> function copies the symbol search path for the specified process into the <i>SearchPath</i> buffer. If the function fails, the contents of the buffer are undefined.

To specify a symbol search path for the process, use the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a> function.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.

To call the Unicode version of this function, define DBGHELP_TRANSLATE_TCHAR.





> [!NOTE]
> The dbghelp.h header defines SymGetSearchPath as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symsetsearchpath">SymSetSearchPath</a>
