---
UID: NF:errhandlingapi.RemoveVectoredExceptionHandler
title: RemoveVectoredExceptionHandler function (errhandlingapi.h)
author: windows-sdk-content
description: Unregisters a vectored exception handler.
old-location: base\removevectoredexceptionhandler.htm
tech.root: Debug
ms.assetid: 94d54b75-e992-477f-ad4f-9b8a3bb44ffb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RemoveVectoredExceptionHandler, RemoveVectoredExceptionHandler function, _win32_removevectoredexceptionhandler, base.removevectoredexceptionhandler, errhandlingapi/RemoveVectoredExceptionHandler
ms.topic: function
req.header: errhandlingapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - RemoveVectoredExceptionHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemoveVectoredExceptionHandler function


## -description


Unregisters a vectored exception handler.


## -parameters




### -param Handle

TBD




#### - Handler [in]

A handle to the vectored exception handler previously registered using the 
<a href="https://msdn.microsoft.com/0e956746-e6da-49d8-a534-753cb6755673">AddVectoredExceptionHandler</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/dbf7016b-09ac-4ca7-9b47-38b0dd763462">Using a Vectored Exception Handler</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0e956746-e6da-49d8-a534-753cb6755673">AddVectoredExceptionHandler</a>



<a href="https://msdn.microsoft.com/e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef">Vectored Exception Handling</a>
 

 

