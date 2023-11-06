---
UID: NS:dbghelp._tagSTACKFRAME64
title: STACKFRAME64 (dbghelp.h)
description: Represents a stack frame. (STACKFRAME64)
helpviewer_keywords: ["*LPSTACKFRAME64","LPSTACKFRAME64","LPSTACKFRAME64 structure pointer","STACKFRAME","STACKFRAME structure","STACKFRAME64","STACKFRAME64 structure","_tagSTACKFRAME64","_win32_stackframe64_str","base.stackframe64_str","dbghelp/LPSTACKFRAME64","dbghelp/STACKFRAME64"]
old-location: base\stackframe64_str.htm
tech.root: Debug
ms.assetid: 2809e3f1-c64a-4753-9fca-f78e89a878b2
ms.date: 12/05/2018
ms.keywords: '*LPSTACKFRAME64, LPSTACKFRAME64, LPSTACKFRAME64 structure pointer, STACKFRAME, STACKFRAME structure, STACKFRAME64, STACKFRAME64 structure, _tagSTACKFRAME64, _win32_stackframe64_str, base.stackframe64_str, dbghelp/LPSTACKFRAME64, dbghelp/STACKFRAME64'
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
req.typenames: STACKFRAME64, *LPSTACKFRAME64
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _tagSTACKFRAME64
 - dbghelp/_tagSTACKFRAME64
 - LPSTACKFRAME64
 - dbghelp/LPSTACKFRAME64
 - STACKFRAME64
 - dbghelp/STACKFRAME64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - STACKFRAME64
 - STACKFRAME
---

# STACKFRAME64 structure


## -description

Represents a stack frame.

## -struct-fields

### -field AddrPC

An 
<a href="/windows/win32/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies the program counter. 




<b>x86:  </b>The program counter is EIP.

<b>Intel Itanium:  </b>The program counter is StIIP.

<b>x64:  </b>The program counter is RIP.

### -field AddrReturn

An 
<a href="/windows/win32/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies the return address.

### -field AddrFrame

An 
<a href="/windows/win32/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies the frame pointer. 




<b>x86:  </b>The frame pointer is EBP.

<b>Intel Itanium:  </b>There is no frame pointer, but <b>AddrBStore</b> is used.

<b>x64:  </b>The frame pointer is RBP or RDI. This value is not always used.

### -field AddrStack

An 
<a href="/windows/win32/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies the stack pointer. 




<b>x86:  </b>The stack pointer is ESP.

<b>Intel Itanium:  </b>The stack pointer is SP.

<b>x64:  </b>The stack pointer is RSP.

### -field AddrBStore

<b>Intel Itanium:  </b>An 
<a href="/windows/win32/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a> structure that specifies the backing store (RsBSP).

### -field FuncTableEntry

On x86 computers, this member is an 
<a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a> structure. If there is no function table entry, this member is <b>NULL</b>.

### -field Params

The possible arguments to the function.

### -field Far

This member is <b>TRUE</b> if this is a WOW far call.

### -field Virtual

This member is <b>TRUE</b> if this is a virtual frame.

### -field Reserved

This member is used internally by the 
<a href="/windows/win32/api/dbghelp/nf-dbghelp-stackwalk64">StackWalk64</a> function.

### -field KdHelp

A 
<a href="/windows/win32/api/dbghelp/ns-dbghelp-kdhelp64">KDHELP64</a> structure that specifies helper data for walking kernel callback frames.

## -remarks

This structure supersedes the <b>STACKFRAME</b> structure. For more information, see 
<a href="/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>STACKFRAME</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define STACKFRAME STACKFRAME64
#define LPSTACKFRAME LPSTACKFRAME64
#else
typedef struct _tagSTACKFRAME {
    ADDRESS     AddrPC;
    ADDRESS     AddrReturn;
    ADDRESS     AddrFrame;
    ADDRESS     AddrStack;
    PVOID       FuncTableEntry;
    DWORD       Params[4];
    BOOL        Far;
    BOOL        Virtual; 
    DWORD       Reserved[3];
    KDHELP      KdHelp;
    ADDRESS     AddrBStore; 
} STACKFRAME, *LPSTACKFRAME;
#endif
```

## -see-also

<a href="/windows/win32/api/dbghelp/ns-dbghelp-address64">ADDRESS64</a>



<a href="/windows/desktop/api/winnt/ns-winnt-fpo_data">FPO_DATA</a>



<a href="/windows/desktop/api/winnt/ns-winnt-image_function_entry">IMAGE_FUNCTION_ENTRY</a>



<a href="/windows/desktop/api/dbghelp/ns-dbghelp-kdhelp">KDHELP64</a>



<a href="/windows/desktop/api/dbghelp/nf-dbghelp-stackwalk">StackWalk64</a>
