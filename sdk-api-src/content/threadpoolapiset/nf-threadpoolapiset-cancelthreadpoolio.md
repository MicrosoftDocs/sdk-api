---
UID: NF:threadpoolapiset.CancelThreadpoolIo
title: CancelThreadpoolIo function (threadpoolapiset.h)
description: Cancels the notification from the StartThreadpoolIo function.
helpviewer_keywords: ["CancelThreadpoolIo","CancelThreadpoolIo function","base.cancelthreadpoolio","threadpoolapiset/CancelThreadpoolIo","winbase/CancelThreadpoolIo"]
old-location: base\cancelthreadpoolio.htm
tech.root: backup
ms.assetid: e3af8313-2e09-4c88-8cef-671efd4228c7
ms.date: 12/05/2018
ms.keywords: CancelThreadpoolIo, CancelThreadpoolIo function, base.cancelthreadpoolio, threadpoolapiset/CancelThreadpoolIo, winbase/CancelThreadpoolIo
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
 - CancelThreadpoolIo
 - threadpoolapiset/CancelThreadpoolIo
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
 - CancelThreadpoolIo
---

# CancelThreadpoolIo function


## -description

Cancels the notification from the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio">StartThreadpoolIo</a> function.

## -parameters

### -param pio [in, out]

A pointer to a <b>TP_IO</b> structure that defines the I/O completion object. The <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a> function returns this pointer.

## -remarks

To prevent memory leaks, you must call the <b>CancelThreadpoolIo</b> function for either of the following scenarios:

<ul>
<li>An overlapped (asynchronous) I/O operation fails (that is, the asynchronous I/O function call returns failure with an error code other than ERROR_IO_PENDING).</li>
<li>An asynchronous I/O operation returns immediately with success and the file handle associated with the I/O completion object has the notification mode FILE_SKIP_COMPLETION_PORT_ON_SUCCESS. The file handle will not notify the I/O completion port and the associated I/O callback function will not be called. </li>
</ul>
To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio">CloseThreadpoolIo</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio">CreateThreadpoolIo</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio">StartThreadpoolIo</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks">WaitForThreadpoolIoCallbacks</a>