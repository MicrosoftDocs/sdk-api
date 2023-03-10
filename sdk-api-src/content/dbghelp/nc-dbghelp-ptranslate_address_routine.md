---
UID: NC:dbghelp.PTRANSLATE_ADDRESS_ROUTINE
title: PTRANSLATE_ADDRESS_ROUTINE (dbghelp.h)
description: PTRANSLATE_ADDRESS_ROUTINE (dbghelp.h) is an application-defined callback function used with the StackWalk64 function.
helpviewer_keywords: ["PTRANSLATE_ADDRESS_ROUTINE","PTRANSLATE_ADDRESS_ROUTINE64","TranslateAddressProc64","TranslateAddressProc64 callback","TranslateAddressProc64 callback function","_win32_translateaddressproc64","base.translateaddressproc64","dbghelp/TranslateAddressProc64"]
old-location: base\translateaddressproc64.htm
tech.root: Debug
ms.assetid: 56c374df-6b48-4649-a914-5cb2f9575bf3
ms.date: 08/04/2022
ms.keywords: PTRANSLATE_ADDRESS_ROUTINE, PTRANSLATE_ADDRESS_ROUTINE64, TranslateAddressProc64, TranslateAddressProc64 callback, TranslateAddressProc64 callback function, _win32_translateaddressproc64, base.translateaddressproc64, dbghelp/TranslateAddressProc64
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - PTRANSLATE_ADDRESS_ROUTINE
 - dbghelp/PTRANSLATE_ADDRESS_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - TranslateAddressProc64
---

# PTRANSLATE_ADDRESS_ROUTINE callback function


## -description

An application-defined callback function used with the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a> function. It provides address translation for 16-bit addresses.

The <b>PTRANSLATE_ADDRESS_ROUTINE64</b> type defines a pointer to this callback function. 
<b>TranslateAddressProc64</b> is a placeholder for the application-defined function name.

## -parameters

### -param hProcess [in]

A handle to the process for which the stack trace is generated.

### -param hThread [in]

A handle to the thread for which the stack trace is generated.

### -param lpaddr [in]

An address to be translated.

## -returns

The function returns the translated address.

## -remarks

This callback function supersedes the <i>PTRANSLATE_ADDRESS_ROUTINE</i> callback function.  <i>PTRANSLATE_ADDRESS_ROUTINE</i> is defined as follows in Dbghelp.h.


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PTRANSLATE_ADDRESS_ROUTINE PTRANSLATE_ADDRESS_ROUTINE64
#else
typedef
DWORD
(__stdcall *PTRANSLATE_ADDRESS_ROUTINE)(
    __in HANDLE hProcess,
    __in HANDLE hThread,
    __out LPADDRESS lpaddr
    );
#endif
```

## -see-also

<a href="/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a>
