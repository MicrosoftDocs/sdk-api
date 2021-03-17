---
UID: NF:winbase.IsBadCodePtr
title: IsBadCodePtr function (winbase.h)
description: Determines whether the calling process has read access to the memory at the specified address.
helpviewer_keywords: ["IsBadCodePtr","IsBadCodePtr function","_win32_isbadcodeptr","base.isbadcodeptr","winbase/IsBadCodePtr"]
old-location: base\isbadcodeptr.htm
tech.root: base
ms.assetid: 001b8972-6a7f-4964-af8d-a6f31ea3a525
ms.date: 12/05/2018
ms.keywords: IsBadCodePtr, IsBadCodePtr function, _win32_isbadcodeptr, base.isbadcodeptr, winbase/IsBadCodePtr
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsBadCodePtr
 - winbase/IsBadCodePtr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - IsBadCodePtr
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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the application is compiled as a debugging version, and the process does not have read access to  the specified memory location, the function causes an assertion and breaks into the debugger. Leaving the debugger, the function continues as usual, and returns a nonzero value. This behavior is by design, as a debugging aid.

## -remarks

In a preemptive multitasking environment, it is possible for some other thread to change the process's access to the memory being tested. Even when the function indicates that the process has read access to the specified memory, you should use structured exception handling when attempting to access the memory. Use of structured exception handling enables the system to notify the process if an access violation exception occurs, giving the process an opportunity to handle the exception.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-isbadreadptr">IsBadReadPtr</a>



<a href="/windows/desktop/api/winbase/nf-winbase-isbadstringptra">IsBadStringPtr</a>



<a href="/windows/desktop/api/winbase/nf-winbase-isbadwriteptr">IsBadWritePtr</a>