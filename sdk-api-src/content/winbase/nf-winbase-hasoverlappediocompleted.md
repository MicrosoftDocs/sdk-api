---
UID: NF:winbase.HasOverlappedIoCompleted
title: HasOverlappedIoCompleted macro
author: windows-sdk-content
description: Provides a high performance test operation that can be used to poll for the completion of an outstanding I/O operation.
old-location: base\hasoverlappediocompleted.htm
tech.root: sync
ms.assetid: 1e2a3bf0-a73e-4406-99ac-32652f7f5b25
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: HasOverlappedIoCompleted, HasOverlappedIoCompleted macro, _win32_hasoverlappediocompleted, base.hasoverlappediocompleted, winbase/HasOverlappedIoCompleted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - HasOverlappedIoCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# HasOverlappedIoCompleted macro


## -description


Provides a high performance test operation that can be used to poll for the completion of an outstanding I/O operation.


## -parameters




### -param lpOverlapped

A pointer to an 
<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that was specified when the overlapped I/O operation was started.


## -remarks



Do not call this macro unless the call to 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_IO_PENDING</b>, indicating that the overlapped I/O has started.

To cancel all pending asynchronous I/O operations, use the 
<a href="base.cancelio">CancelIo</a> function. The <b>CancelIo</b> function only cancels operations issued by the calling thread for the specified file handle. I/O operations that are canceled complete with the error <b>ERROR_OPERATION_ABORTED</b>.

To get more details about a completed I/O operation, call the 
<a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or 
<a href="base.getqueuedcompletionstatus">GetQueuedCompletionStatus</a> function.




## -see-also




<a href="base.cancelio">CancelIo</a>



<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="base.readfile">ReadFile</a>



<a href="https://msdn.microsoft.com/79afcb18-babb-453e-8618-81b43ecb24c4">TransactNamedPipe</a>



<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a>



<a href="base.writefile">WriteFile</a>
 

 

