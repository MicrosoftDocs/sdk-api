---
UID: NF:threadpoolapiset.WaitForThreadpoolIoCallbacks
title: WaitForThreadpoolIoCallbacks function (threadpoolapiset.h)
description: Waits for outstanding I/O completion callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.helpviewer_keywords: ["WaitForThreadpoolIoCallbacks","WaitForThreadpoolIoCallbacks function","base.waitforthreadpooliocallbacks","threadpoolapiset/WaitForThreadpoolIoCallbacks","winbase/WaitForThreadpoolIoCallbacks"]
old-location: base\waitforthreadpooliocallbacks.htm
tech.root: ProcThread
ms.assetid: 68dc640d-8678-441d-88bd-01284d98a251
ms.date: 12/05/2018
ms.keywords: WaitForThreadpoolIoCallbacks, WaitForThreadpoolIoCallbacks function, base.waitforthreadpooliocallbacks, threadpoolapiset/WaitForThreadpoolIoCallbacks, winbase/WaitForThreadpoolIoCallbacks
f1_keywords:
- threadpoolapiset/WaitForThreadpoolIoCallbacks
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WaitForThreadpoolIoCallbacks function


## -description


Waits for outstanding I/O completion callbacks to complete and optionally cancels pending callbacks that have not yet started to execute.


## -parameters




### -param pio [in, out]

A <b>TP_IO</b> structure that defines the I/O completion object. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a> function returns this structure.


### -param fCancelPendingCallbacks [in]

Indicates whether to cancel queued callbacks that have not yet started to execute.


## -remarks



When <i>fCancelPendingCallbacks</i> is set to TRUE, only queued callbacks are canceled. Pending I/O requests are not canceled. Therefore, the caller should call <a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> for the <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure to check whether the I/O operation has completed before freeing the structure. As an alternative, set <i>fCancelPendingCallbacks</i> to FALSE and have the associated I/O completion callback free the <b>OVERLAPPED</b> structure. Be careful not to free the <b>OVERLAPPED</b> structure while I/O requests are still pending; use <b>GetOverlappedResult</b> to determine the status of the I/O operation and wait for the operation to complete. The <a href="https://docs.microsoft.com/windows/desktop/FileIO/cancelioex-func">CancelIoEx</a> function can optionally be used first to cancel outstanding I/O requests, potentially shortening the wait. For more information, see <a href="https://docs.microsoft.com/windows/desktop/FileIO/canceling-pending-i-o-operations">Canceling Pending I/O Operations</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio">CloseThreadpoolIo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio">StartThreadpoolIo</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>
 

 

