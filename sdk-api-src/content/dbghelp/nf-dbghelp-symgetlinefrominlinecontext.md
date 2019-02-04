---
UID: NF:dbghelp.SymGetLineFromInlineContext
title: SymGetLineFromInlineContext function
author: windows-sdk-content
description: Locates the source line for the specified inline context.
old-location: base\symgetlinefrominlinecontext.htm
tech.root: Debug
ms.assetid: 0c362bd9-7496-436b-9e01-2054dc3dfc57
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SymGetLineFromInlineContext, SymGetLineFromInlineContext function, SymGetLineFromInlineContextW, base.symgetlinefrominlinecontext, dbghelp/SymGetLineFromInlineContext, dbghelp/SymGetLineFromInlineContextW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.2 or later
---

# SymGetLineFromInlineContext function


## -description


Locates the source line for the specified inline context.


## -parameters




### -param hProcess [in]

A handle to the process that was originally passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param qwAddr

TBD


### -param InlineContext [in]

The inline context.


### -param qwModuleBaseAddress [in, optional]

The base address of the module.


### -param pdwDisplacement [out]

The displacement in bytes from the beginning of the line, or zero.


### -param Line64

TBD




#### - Line [out]

A pointer to an <a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> 
      structure.


#### - dwAddr [in]

The address for which a line should be located. It is not necessary for the address to be on a line 
      boundary. If the address appears after the beginning of a line and before the end of the line, the line is 
      found.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The caller must allocate the <i>Line</i> buffer properly and fill in the required members 
    of the <a href="https://msdn.microsoft.com/62124983-8381-4eb4-94f6-220b844aca45">IMAGEHLP_LINE64</a> structure before 
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

<pre class="syntax" xml:space="preserve"><code>BOOL
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
#endif</code></pre>


