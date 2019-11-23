---
UID: NF:threadpoolapiset.CloseThreadpoolIo
title: CloseThreadpoolIo function (threadpoolapiset.h)

description: Releases the specified I/O completion object.
old-location: base\closethreadpoolio.htm
tech.root: ProcThread
ms.assetid: 499190de-54e8-4be6-909b-04505bcb0aa6

ms.date: 12/05/2018
ms.keywords: CloseThreadpoolIo, CloseThreadpoolIo function, base.closethreadpoolio, threadpoolapiset/CloseThreadpoolIo, winbase/CloseThreadpoolIo
ms.topic: function
f1_keywords: 
 - "threadpoolapiset/CloseThreadpoolIo"
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
 - CloseThreadpoolIo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseThreadpoolIo function


## -description


Releases the specified I/O completion object.


## -parameters




### -param pio [in, out]

A <b>TP_IO</b> structure that defines the I/O completion object. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



The I/O completion object is freed immediately if there are no outstanding callbacks; otherwise, the I/O completion object is freed asynchronously after the outstanding callbacks complete. 

You should close the associated file handle and wait for all outstanding overlapped I/O operations to complete before calling this function—you must not cause any more overlapped I/O operations to occur after calling this function.

It may be necessary to cancel threadpool I/O notifications to prevent memory leaks. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio">StartThreadpoolIo</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks">WaitForThreadpoolIoCallbacks</a>
 

 

