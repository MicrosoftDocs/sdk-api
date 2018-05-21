---
UID: NF:winnt.RtlRestoreContext
title: RtlRestoreContext function
author: windows-driver-content
description: Restores the context of the caller to the specified context record.
old-location: base\rtlrestorecontext.htm
old-project: Debug
ms.assetid: f5304d17-bc67-4e0f-a535-efca4e65c74c
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: RtlRestoreContext, RtlRestoreContext function, base.rtlrestorecontext, winnt/RtlRestoreContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: TRANSACTION_OUTCOME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-rtlsupport-l1-1-0.dll
-	ntdll.dll
-	API-MS-Win-Core-rtlsupport-l1-2-0.dll
api_name:
-	RtlRestoreContext
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of Windows Server 2003
---

# RtlRestoreContext function


## -description


Restores the context of the caller to the specified context record.


## -parameters




### -param ContextRecord [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> structure.


### -param ExceptionRecord [in]

A pointer to an <a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a> structure. This parameter is optional and should typically be <b>NULL</b>. 

An exception record is used primarily with long jump and C++ catch-throw support. If the <b>ExceptionCode</b> member is STATUS_LONGJUMP, the <b>ExceptionInformation</b> member contains a pointer to a jump buffer. <b>RtlRestoreContext</b> will copy the non-volatile state from the jump buffer in to the context record before the context record is restored.

If the <b>ExceptionCode</b> member is STATUS_UNWIND_CONSOLIDATE, the <b>ExceptionInformation</b> member contains a pointer to a callback function, such as a catch handler. <b>RtlRestoreContext</b> consolidates the call frames between its frame and the frame specified in the context record before calling the callback function. This hides frames from any exception handling that might occur in the callback function. The difference between this and a typical unwind is that the data on the stack is still present, so frame data such as a throw object is still available. The callback function returns a new program counter to update in the context record, which is then used in a normal restore context.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552116">RtlCaptureContext</a>
 

 

