---
UID: NF:dbghelp.SymGetLineFromInlineContextW
title: SymGetLineFromInlineContextW function (dbghelp.h)
description: The SymGetLineFromInlineContextW (Unicode) function locates the source line for the specified inline context.
helpviewer_keywords: ["SymGetLineFromInlineContext","SymGetLineFromInlineContext function","SymGetLineFromInlineContextW","base.symgetlinefrominlinecontext","dbghelp/SymGetLineFromInlineContext","dbghelp/SymGetLineFromInlineContextW"]
old-location: base\symgetlinefrominlinecontext.htm
tech.root: Debug
ms.assetid: 0c362bd9-7496-436b-9e01-2054dc3dfc57
ms.date: 08/04/2022
ms.keywords: SymGetLineFromInlineContext, SymGetLineFromInlineContext function, SymGetLineFromInlineContextW, base.symgetlinefrominlinecontext, dbghelp/SymGetLineFromInlineContext, dbghelp/SymGetLineFromInlineContextW
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SymGetLineFromInlineContextW (Unicode) and SymGetLineFromInlineContext (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
ms.custom: 19H1
f1_keywords:
 - SymGetLineFromInlineContextW
 - dbghelp/SymGetLineFromInlineContextW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - DbgHelp.dll
api_name:
 - SymGetLineFromInlineContext
 - SymGetLineFromInlineContext
 - SymGetLineFromInlineContextW
---

## -description

Locates the source line for the specified inline context.

## -parameters

### -param hProcess [in]

A handle to the process that was originally passed to the 
      <a href="/windows/desktop/api/dbghelp/nf-dbghelp-syminitialize">SymInitialize</a> function.

### -param dwAddr [in]

The address for which a line should be located. It is not necessary for the address to be on a line 
      boundary. If the address appears after the beginning of a line and before the end of the line, the line is 
      found.

### -param InlineContext [in]

The inline context.

### -param qwModuleBaseAddress [in, optional]

The base address of the module.

### -param pdwDisplacement [out]

The displacement in bytes from the beginning of the line, or zero.

### -param Line [out]

A pointer to an <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> 
      structure.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller must allocate the <i>Line</i> buffer properly and fill in the required members 
    of the <a href="/windows/desktop/api/dbghelp/ns-dbghelp-imagehlp_line">IMAGEHLP_LINE64</a> structure before 
    calling <b>SymGetLineFromInlineContext</b>.

This function returns a pointer to a buffer that may be reused by another function. Therefore, be sure to copy 
    the data returned to another buffer immediately.

All DbgHelp functions, such as this one, are single 
    threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or 
    memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this 
    function.

To call the Unicode version of this function, define <b>DBGHELP_TRANSLATE_TCHAR</b>. 
    <b>SymGetLineFromInlineContext</b> is defined as 
    follows in Dbghelp.h.


``` syntax
BOOL
IMAGEAPI
SymGetLineFromInlineContextW(
    _In_ HANDLE hProcess,
    _In_ DWORD64 dwAddr,
    _In_ ULONG InlineContext,
    _In_opt_ DWORD64 qwModuleBaseAddress,
    _Out_ PDWORD pdwDisplacement,
    _Out_ PIMAGEHLP_LINEW64 Line
    );

#ifdef DBGHELP_TRANSLATE_TCHAR
 #define SymGetLineFromInlineContext SymGetLineFromInlineContextW
#endif
```




> [!NOTE]
> The dbghelp.h header defines SymGetLineFromInlineContext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
