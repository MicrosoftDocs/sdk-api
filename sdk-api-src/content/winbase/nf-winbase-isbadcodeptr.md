---
UID: NF:winbase.IsBadCodePtr
title: IsBadCodePtr function
author: windows-sdk-content
description: Determines whether the calling process has read access to the memory at the specified address.
old-location: base\isbadcodeptr.htm
tech.root: memory
ms.assetid: 001b8972-6a7f-4964-af8d-a6f31ea3a525
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IsBadCodePtr, IsBadCodePtr function, _win32_isbadcodeptr, base.isbadcodeptr, winbase/IsBadCodePtr
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
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
api_name:
 - IsBadCodePtr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsBadCodePtr function


## -description


Determines whether the calling process has read access to the memory at the specified address.
<div class="alert"><b>Important</b>  This function is obsolete and should not be used. Despite its name, it does not guarantee that the pointer is valid or that the memory pointed to is safe to use. For more information, see Remarks on this page.</div><div> </div>

## -parameters




### -param lpfn [in]

A pointer to a memory address.


## -returns



If the calling process has read access to the specified memory, the return value is zero.

If the calling process does not have read access to the specified memory, the return value is nonzero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the application is compiled as a debugging version, and the process does not have read access to  the specified memory location, the function causes an assertion and breaks into the debugger. Leaving the debugger, the function continues as usual, and returns a nonzero value. This behavior is by design, as a debugging aid.




## -remarks



In a preemptive multitasking environment, it is possible for some other thread to change the process's access to the memory being tested. Even when the function indicates that the process has read access to the specified memory, you should use structured exception handling when attempting to access the memory. Use of structured exception handling enables the system to notify the process if an access violation exception occurs, giving the process an opportunity to handle the exception.




## -see-also




<a href="https://msdn.microsoft.com/c1561403-2b77-4c93-80f1-261f26629d4b">IsBadReadPtr</a>



<a href="https://msdn.microsoft.com/ec708f97-36c8-4484-96d7-b8dfb8578667">IsBadStringPtr</a>



<a href="https://msdn.microsoft.com/2b353a8e-45cf-4108-9522-bcbde9c71ec4">IsBadWritePtr</a>
 

 

