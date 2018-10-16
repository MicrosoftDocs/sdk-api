---
UID: NF:threadpoolapiset.WaitForThreadpoolIoCallbacks
title: WaitForThreadpoolIoCallbacks function
author: windows-sdk-content
description: Waits for outstanding I/O completion callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.
old-location: base\waitforthreadpooliocallbacks.htm
tech.root: procthread
ms.assetid: 68dc640d-8678-441d-88bd-01284d98a251
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: WaitForThreadpoolIoCallbacks, WaitForThreadpoolIoCallbacks function, base.waitforthreadpooliocallbacks, threadpoolapiset/WaitForThreadpoolIoCallbacks, winbase/WaitForThreadpoolIoCallbacks
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - WaitForThreadpoolIoCallbacks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WaitForThreadpoolIoCallbacks function


## -description


Waits for outstanding I/O completion callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.


## -parameters




### -param pio [in, out]

A <b>TP_IO</b> structure that defines the I/O completion object. The <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a> function returns this structure.


### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.


## -returns



This function does not return a value.




## -remarks



When <i>fCancelPendingCallbacks</i> is set to TRUE, only queued callbacks are canceled. Pending I/O requests are not canceled. Therefore, the caller should call <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> for the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure to check whether the I/O operation has completed before freeing the structure. As an alternative, set <i>fCancelPendingCallbacks</i> to FALSE and have the associated I/O completion callback free the <b>OVERLAPPED</b> structure. Be careful not to free the <b>OVERLAPPED</b> structure while I/O requests are still pending; use <b>GetOverlappedResult</b> to determine the status of the I/O operation and wait for the operation to complete. The <a href="https://msdn.microsoft.com/a2ce13b8-7da6-4848-848d-901d9667c2e3">CancelIoEx</a> function can optionally be used first to cancel outstanding I/O requests, potentially shortening the wait. For more information, see <a href="https://msdn.microsoft.com/adfe6d05-f30b-40a1-b3b0-58e2593e7b25">Canceling Pending I/O Operations</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a>



<a href="https://msdn.microsoft.com/499190de-54e8-4be6-909b-04505bcb0aa6">CloseThreadpoolIo</a>



<a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a>



<a href="https://msdn.microsoft.com/5a817d6f-a8e6-4aaa-b560-0128eacb98b1">StartThreadpoolIo</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

