---
UID: NS:dbghelp._KDHELP
title: KDHELP (dbghelp.h)
description: Information that is used by kernel debuggers to trace through user-mode callbacks in a thread's kernel stack.
helpviewer_keywords: ["*PKDHELP","KDHELP","KDHELP structure","KDHELP64","KDHELP64 structure","PKDHELP64","PKDHELP64 structure pointer","_KDHELP64","_win32_kdhelp64_str","base.kdhelp64_str","dbghelp/KDHELP64","dbghelp/PKDHELP64"]
old-location: base\kdhelp64_str.htm
tech.root: Debug
ms.assetid: da31c92c-0257-4ae2-8d69-ea8cd58adc10
ms.date: 12/05/2018
ms.keywords: '*PKDHELP, KDHELP, KDHELP structure, KDHELP64, KDHELP64 structure, PKDHELP64, PKDHELP64 structure pointer, _KDHELP64, _win32_kdhelp64_str, base.kdhelp64_str, dbghelp/KDHELP64, dbghelp/PKDHELP64'
f1_keywords:
- dbghelp/KDHELP64
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
- KDHELP64
- KDHELP
targetos: Windows
req.typenames: KDHELP, *PKDHELP
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# KDHELP structure


## -description


Information that is used by kernel debuggers to trace through user-mode callbacks in a thread's kernel stack.


## -struct-fields




### -field Thread

The address of the kernel thread object, as provided in the WAIT_STATE_CHANGE packet.


### -field ThCallbackStack

The offset in the thread object to the pointer to the current callback frame in the kernel stack.


### -field NextCallback

The address of the next callback frame.


### -field FramePointer

The address of the saved frame pointer, if applicable.


### -field KiCallUserMode

The address of the kernel function that calls out to user mode.


### -field KeUserCallbackDispatcher

The address of the user-mode dispatcher function.


### -field SystemRangeStart

The lowest kernel-mode address.


### -field ThCallbackBStore

<b>Intel Itanium:  </b>The offset in the thread object to a pointer to the current callback backing store frame in the kernel stack.


### -field KiUserExceptionDispatcher

The address of the user-mode exception dispatcher function.

<b>DbgHelp 6.1 and earlier:  </b>This member is not supported.


### -field StackBase

The address of the stack base.


### -field StackLimit

The stack limit.


### -field Reserved

This member is reserved for use by the operating system.


## -remarks



This structure supersedes the <b>KDHELP</b> structure. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/Debug/updated-platform-support">Updated Platform Support</a>. <b>KDHELP</b> is defined as follows in Dbghelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define KDHELP KDHELP64
#define PKDHELP PKDHELP64
#else
typedef struct _KDHELP {
    DWORD   Thread;
    DWORD   ThCallbackStack;
    DWORD   NextCallback;
    DWORD   FramePointer;
    DWORD   KiCallUserMode;
    DWORD   KeUserCallbackDispatcher;
    DWORD   SystemRangeStart;
    DWORD   ThCallbackBStore;
    DWORD   KiUserExceptionDispatcher;
    DWORD   StackBase;
    DWORD   StackLimit;
    DWORD   Reserved[5];
} KDHELP, *PKDHELP;
#endif
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-stackframe">STACKFRAME64</a>
 

 

