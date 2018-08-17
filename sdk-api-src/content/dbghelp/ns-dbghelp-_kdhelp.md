---
UID: NS:dbghelp._KDHELP
title: "_KDHELP"
author: windows-sdk-content
description: Information that is used by kernel debuggers to trace through user-mode callbacks in a thread's kernel stack.
old-location: base\kdhelp64_str.htm
old-project: debug
ms.assetid: da31c92c-0257-4ae2-8d69-ea8cd58adc10
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PKDHELP, KDHELP, KDHELP structure, KDHELP64, KDHELP64 structure, PKDHELP64, PKDHELP64 structure pointer, _KDHELP, _KDHELP64, _win32_kdhelp64_str, base.kdhelp64_str, dbghelp/KDHELP64, dbghelp/PKDHELP64"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 5.1 or later
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
tech.root: 
req.typenames: KDHELP, *PKDHELP
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _KDHELP structure


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
<a href="https://msdn.microsoft.com/34ec8cd3-3260-441d-b55f-4ea21c736eb1">Updated Platform Support</a>. <b>KDHELP</b> is defined as follows in Dbghelp.h. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#if !defined(_IMAGEHLP_SOURCE_) &amp;&amp; defined(_IMAGEHLP64)
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
#endif</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2809e3f1-c64a-4753-9fca-f78e89a878b2">STACKFRAME64</a>
 

 

