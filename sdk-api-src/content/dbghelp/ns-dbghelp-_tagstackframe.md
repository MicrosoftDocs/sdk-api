---
UID: NS:dbghelp._tagSTACKFRAME
title: "_tagSTACKFRAME"
author: windows-sdk-content
description: Represents a stack frame.
old-location: base\stackframe64_str.htm
tech.root: debug
ms.assetid: 2809e3f1-c64a-4753-9fca-f78e89a878b2
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: "*LPSTACKFRAME, LPSTACKFRAME64, LPSTACKFRAME64 structure pointer, STACKFRAME, STACKFRAME structure, STACKFRAME64, STACKFRAME64 structure, _tagSTACKFRAME, _tagSTACKFRAME64, _win32_stackframe64_str, base.stackframe64_str, dbghelp/LPSTACKFRAME64, dbghelp/STACKFRAME64"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: STACKFRAME, *LPSTACKFRAME
req.redist: DbgHelp.dll 5.1 or later
---

# _tagSTACKFRAME structure


## -description


Represents a stack frame.


## -struct-fields




### -field AddrPC

An 
<a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies the program counter. 




<b>x86:  </b>The program counter is EIP.

<b>Intel Itanium:  </b>The program counter is StIIP.

<b>x64:  </b>The program counter is RIP.


### -field AddrReturn

An 
<a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies the return address.


### -field AddrFrame

An 
<a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies the frame pointer. 




<b>x86:  </b>The frame pointer is EBP.

<b>Intel Itanium:  </b>There is no frame pointer, but <b>AddrBStore</b> is used.

<b>x64:  </b>The frame pointer is RBP or RDI. This value is not always used.


### -field AddrStack

An 
<a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies the stack pointer. 




<b>x86:  </b>The stack pointer is ESP.

<b>Intel Itanium:  </b>The stack pointer is SP.

<b>x64:  </b>The stack pointer is RSP.


### -field FuncTableEntry

On x86 computers, this member is an 
<a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a> structure. If there is no function table entry, this member is <b>NULL</b>.


### -field Params

The possible arguments to the function.


### -field Far

This member is <b>TRUE</b> if this is a WOW far call.


### -field Virtual

This member is <b>TRUE</b> if this is a virtual frame.


### -field Reserved

This member is used internally by the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function.


### -field KdHelp

A 
<a href="https://msdn.microsoft.com/da31c92c-0257-4ae2-8d69-ea8cd58adc10">KDHELP64</a> structure that specifies helper data for walking kernel callback frames.


### -field AddrBStore

<b>Intel Itanium:  </b>An 
<a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a> structure that specifies the backing store (RsBSP).


## -remarks



This structure supersedes the <b>STACKFRAME</b> structure. For more information, see 
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>STACKFRAME</b> is defined as follows in Dbghelp.h. 


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




<a href="https://msdn.microsoft.com/f49249e5-ef02-4e1f-9c08-1c7fe25ee71c">ADDRESS64</a>



<a href="https://msdn.microsoft.com/916dc7d5-ed88-4573-b696-fd00bbf4e086">FPO_DATA</a>



<a href="https://msdn.microsoft.com/ced956ec-7a12-4548-8e38-a1c1057c05e8">IMAGE_FUNCTION_ENTRY</a>



<a href="https://msdn.microsoft.com/da31c92c-0257-4ae2-8d69-ea8cd58adc10">KDHELP64</a>



<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a>
 

 

