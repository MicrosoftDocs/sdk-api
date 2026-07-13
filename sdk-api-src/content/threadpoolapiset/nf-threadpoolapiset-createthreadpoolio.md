---
UID: NF:threadpoolapiset.CreateThreadpoolIo
title: CreateThreadpoolIo function (threadpoolapiset.h)
description: Creates a new I/O completion object.
helpviewer_keywords: ["CreateThreadpoolIo","CreateThreadpoolIo function","base.createthreadpoolio","threadpoolapiset/CreateThreadpoolIo","winbase/CreateThreadpoolIo"]
old-location: base\createthreadpoolio.htm
tech.root: backup
ms.assetid: 621f4747-50fa-4538-bd6a-dbe4dbb05dd1
ms.date: 12/05/2018
ms.keywords: CreateThreadpoolIo, CreateThreadpoolIo function, base.createthreadpoolio, threadpoolapiset/CreateThreadpoolIo, winbase/CreateThreadpoolIo
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
 - CreateThreadpoolIo
 - threadpoolapiset/CreateThreadpoolIo
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
 - CreateThreadpoolIo
---

# CreateThreadpoolIo function


## -description

Creates a new I/O completion object.

## -parameters

### -param fl [in]

The file handle to bind to this I/O completion object.

### -param pfnio [in]

The callback function to be called each time  an overlapped I/O operation completes on the file. For details, see <a href="/previous-versions/windows/desktop/legacy/ms684124(v=vs.85)">IoCompletionCallback</a>.

### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.

### -param pcbe [in, optional]

A pointer to a <b>TP_CALLBACK_ENVIRON</b> structure that defines the environment in which to execute the callback. Use the <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a> function to initialize the structure before calling this function.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="/windows/desktop/api/winbase/nf-winbase-initializethreadpoolenvironment">InitializeThreadpoolEnvironment</a>.

## -returns

If the function succeeds, it returns a pointer to a <b>TP_IO</b> structure that defines the I/O object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To begin receiving overlapped I/O completion callbacks, call the <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio">StartThreadpoolIo</a> function.

If the file handle bound to the I/O completion object has the notification mode FILE_SKIP_COMPLETION_PORT_ON_SUCCESS and an asychronous I/O operation returns immediately with success, the I/O completion callback function is not called and threadpool I/O notifications must be canceled. For more information, see <a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a>.   

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.

## -see-also

<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-cancelthreadpoolio">CancelThreadpoolIo</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-closethreadpoolio">CloseThreadpoolIo</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-startthreadpoolio">StartThreadpoolIo</a>



<a href="/windows/desktop/ProcThread/thread-pools">Thread Pools</a>



<a href="/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-waitforthreadpooliocallbacks">WaitForThreadpoolIoCallbacks</a>