---
UID: NF:winbase.IsBadStringPtrW
title: IsBadStringPtrW function
author: windows-driver-content
description: Verifies that the calling process has read access to the specified range of memory.
old-location: base\isbadstringptr.htm
old-project: Memory
ms.assetid: ec708f97-36c8-4484-96d7-b8dfb8578667
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IsBadStringPtr, IsBadStringPtr function, IsBadStringPtrA, IsBadStringPtrW, _win32_isbadstringptr, base.isbadstringptr, winbase/IsBadStringPtr, winbase/IsBadStringPtrA, winbase/IsBadStringPtrW
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
req.unicode-ansi: IsBadStringPtrW (Unicode) and IsBadStringPtrA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
api_name:
-	IsBadStringPtr
-	IsBadStringPtrA
-	IsBadStringPtrW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IsBadStringPtrW function


## -description


Verifies that the calling process has read access to the specified range of memory.
<div class="alert"><b>Important</b>  This function is obsolete and should not be used. Despite its name, it does not guarantee that the pointer is valid or that the memory pointed to is safe to use. For more information, see Remarks on this page.</div><div> </div>

## -parameters




### -param lpsz [in]

A pointer to a null-terminated string, either Unicode or ASCII.


### -param ucchMax [in]

The maximum size of the string, in <b>TCHARs</b>. The function checks for read access in all characters up to the string's terminating null character or up to the number of characters specified by this parameter, whichever is smaller. If this parameter is zero, the return value is zero.


## -returns



If the calling process has read access to all characters up to the string's terminating null character or up to the number of characters specified by <i>ucchMax</i>, the return value is zero.

If the calling process does not have read access to all characters up to the string's terminating null character or up to the number of characters specified by <i>ucchMax</i>, the return value is nonzero.

If the application is compiled as a debugging version, and the process does not have read access to the entire memory range specified, the function causes an assertion and breaks into the debugger. Leaving the debugger, the function continues as usual, and returns a nonzero value This behavior is by design, as a debugging aid.




## -remarks



This function is typically used when working with pointers returned from third-party libraries, where you cannot determine the memory management behavior in the third-party DLL.

Threads in a process are expected to cooperate in such a way that one will not free memory that the other needs. Use of this function does not negate the need to do this. If this is not done, the application may fail in an unpredictable manner.

Dereferencing potentially invalid pointers can disable stack expansion in other threads. A thread exhausting its stack, when stack expansion has been disabled, results in the immediate termination of the parent process, with no pop-up error window or diagnostic information.

If the calling process has read access to some, but not all, of the specified memory range, the return value is nonzero.

In a preemptive multitasking environment, it is possible for some other thread to change the process's access to the memory being tested. Even when the function indicates that the process has read access to the specified memory, you should use 
<a href="https://msdn.microsoft.com/6b6326d8-6875-4146-a4e3-7873f4e400cb">structured exception handling</a> when attempting to access the memory. Use of structured exception handling enables the system to notify the process if an access violation exception occurs, giving the process an opportunity to handle the exception.




## -see-also




<a href="https://msdn.microsoft.com/001b8972-6a7f-4964-af8d-a6f31ea3a525">IsBadCodePtr</a>



<a href="https://msdn.microsoft.com/c1561403-2b77-4c93-80f1-261f26629d4b">IsBadReadPtr</a>



<a href="https://msdn.microsoft.com/2b353a8e-45cf-4108-9522-bcbde9c71ec4">IsBadWritePtr</a>
 

 

