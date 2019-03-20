---
UID: NC:dbghelp.PGET_MODULE_BASE_ROUTINE64
title: PGET_MODULE_BASE_ROUTINE64 (dbghelp.h)
author: windows-sdk-content
description: An application-defined callback function used with the StackWalk64 function. It is called when StackWalk64 needs a module base address for a given virtual address.
old-location: base\getmodulebaseproc64.htm
tech.root: Debug
ms.assetid: a1060d41-183f-4cb1-8214-afef2996ca66
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetModuleBaseProc64, GetModuleBaseProc64 callback, GetModuleBaseProc64 callback function, PGET_MODULE_BASE_ROUTINE, PGET_MODULE_BASE_ROUTINE64, _win32_getmodulebaseproc64, base.getmodulebaseproc64, dbghelp/GetModuleBaseProc64
ms.topic: callback
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
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - GetModuleBaseProc64
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# PGET_MODULE_BASE_ROUTINE64 callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a> function. It is called when 
<b>StackWalk64</b> needs a module base address for a given virtual address.

The <b>PGET_MODULE_BASE_ROUTINE64</b> type defines a pointer to this callback function. 
<b>GetModuleBaseProc64</b> is a placeholder for the application-defined function name.


## -parameters




### -param hProcess [in]

A handle to the process for which the stack trace is generated.


### -param Address [in]

An address within the module image to be located.


## -returns



The function returns the base address of the module.




## -remarks



This callback function supersedes the <i>PGET_MODULE_BASE_ROUTINE</i> callback function.  <i>PGET_MODULE_BASE_ROUTINE</i> is defined as follows in DbgHelp.h. 


```cpp
#if !defined(_IMAGEHLP_SOURCE_) && defined(_IMAGEHLP64)
#define PGET_MODULE_BASE_ROUTINE PGET_MODULE_BASE_ROUTINE64
#else
typedef
DWORD
(__stdcall *PGET_MODULE_BASE_ROUTINE)(
    __in HANDLE hProcess,
    __in DWORD Address
    );
#endif
```





## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/e2bdaa4c-5474-41a0-bcea-927570c8402c">StackWalk64</a>
 

 

