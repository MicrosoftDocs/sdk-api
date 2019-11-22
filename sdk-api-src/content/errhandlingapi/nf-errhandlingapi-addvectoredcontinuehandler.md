---
UID: NF:errhandlingapi.AddVectoredContinueHandler
title: AddVectoredContinueHandler function (errhandlingapi.h)

description: Registers a vectored continue handler.
old-location: base\addvectoredcontinuehandler.htm
tech.root: Debug
ms.assetid: 23ad21a1-a298-45ac-9867-463f0852f292

ms.date: 12/05/2018
ms.keywords: AddVectoredContinueHandler, AddVectoredContinueHandler function, base.addvectoredcontinuehandler, errhandlingapi/AddVectoredContinueHandler
ms.topic: function
f1_keywords: 
 - "errhandlingapi/AddVectoredContinueHandler"
dev_langs:
 - c++
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP Professional x64 Edition [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-errorhandling-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-errorhandling-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ErrorHandling-L1-1-3.dll
api_name:
 - AddVectoredContinueHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AddVectoredContinueHandler function


## -description


Registers a vectored continue handler.


## -parameters




### -param First

TBD


### -param Handler

TBD




#### - FirstHandler [in]

The order in which the handler should be called. If the parameter is nonzero, the handler is the first handler to be called. If the parameter is zero, the handler is the last handler to be called.


#### - VectoredHandler [in]

A pointer to the handler to be called. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-pvectored_exception_handler">VectoredHandler</a>.


## -returns



If the function succeeds, the return value is a pointer to the exception handler.

If the function fails, the return value is <b>NULL</b>.




## -remarks



If the <i>FirstHandler</i> parameter is nonzero, the handler is the first handler to be called until a subsequent call to 
<b>AddVectoredContinueHandler</b> is used to specify a different handler as the first handler.

If the <i>VectoredHandler</i> parameter points to a function in a DLL and that DLL is unloaded, the handler is still registered. This can lead to application errors.

To unregister the handler, use the 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler">RemoveVectoredContinueHandler</a> function.

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler">AddVectoredExceptionHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler">RemoveVectoredContinueHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/Debug/vectored-exception-handling">Vectored Exception Handling</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/nc-winnt-pvectored_exception_handler">VectoredHandler</a>
 

 

