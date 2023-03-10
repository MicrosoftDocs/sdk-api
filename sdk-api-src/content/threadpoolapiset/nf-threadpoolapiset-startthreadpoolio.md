---
UID: NF:threadpoolapiset.StartThreadpoolIo
title: StartThreadpoolIo function (threadpoolapiset.h)
description: Notifies the thread pool that I/O operations may possibly begin for the specified I/O completion object. A worker thread calls the I/O completion object's callback function after the operation completes on the file handle bound to this object.
helpviewer_keywords: ["StartThreadpoolIo","StartThreadpoolIo function","base.startthreadpoolio","threadpoolapiset/StartThreadpoolIo","winbase/StartThreadpoolIo"]
old-location: base\startthreadpoolio.htm
tech.root: backup
ms.assetid: 5a817d6f-a8e6-4aaa-b560-0128eacb98b1
ms.date: 12/05/2018
ms.keywords: StartThreadpoolIo, StartThreadpoolIo function, base.startthreadpoolio, threadpoolapiset/StartThreadpoolIo, winbase/StartThreadpoolIo
req.header: threadpoolapiset.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StartThreadpoolIo
 - threadpoolapiset/StartThreadpoolIo
dev_langs:
 - c++
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
 - StartThreadpoolIo
---

# StartThreadpoolIo function


## -description

Notifies the thread pool that I/O operations may possibly begin for the specified I/O completion object. A worker thread calls the I/O completion object's callback function after the operation completes on the file handle bound to this object.

## -parameters

### -param pio [in, out]

A pointer to a <b>TP_IO</b> structure that defines the I/O completion object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a> function returns this pointer.

## -remarks

You must call this function before initiating each asynchronous I/O operation on the file handle bound to the I/O completion object. Failure to do so will cause the thread pool to ignore an I/O operation when it completes and will cause memory corruption.

If the I/O operation fails, call the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a> function to cancel this notification.

If the file handle bound to the I/O completion object has the notification mode FILE_SKIP_COMPLETION_PORT_ON_SUCCESS and an asynchronous I/O operation returns immediately with success, the object's I/O completion callback function is not called and threadpool I/O notifications must be canceled. For more information, see  <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a>.   

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio">CloseThreadpoolIo</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks">WaitForThreadpoolIoCallbacks</a>