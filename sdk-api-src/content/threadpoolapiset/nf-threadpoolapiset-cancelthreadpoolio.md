---
UID: NF:threadpoolapiset.CancelThreadpoolIo
title: CancelThreadpoolIo function (threadpoolapiset.h)
author: windows-sdk-content
description: Cancels the notification from the StartThreadpoolIo function.
old-location: base\cancelthreadpoolio.htm
tech.root: ProcThread
ms.assetid: e3af8313-2e09-4c88-8cef-671efd4228c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CancelThreadpoolIo, CancelThreadpoolIo function, base.cancelthreadpoolio, threadpoolapiset/CancelThreadpoolIo, winbase/CancelThreadpoolIo
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
 - CancelThreadpoolIo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CancelThreadpoolIo function


## -description


Cancels the notification from the <a href="https://msdn.microsoft.com/5a817d6f-a8e6-4aaa-b560-0128eacb98b1">StartThreadpoolIo</a> function.


## -parameters




### -param pio [in, out]

A <b>TP_IO</b> structure that defines the I/O completion object. The <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



To prevent memory leaks, you must call the <b>CancelThreadpoolIo</b> function for either of the following scenarios:

<ul>
<li>An overlapped (asynchronous) I/O operation fails (that is, the asynchronous I/O function call returns failure with an error code other than ERROR_IO_PENDING).</li>
<li>An asynchronous I/O operation returns immediately with success and the file handle associated with the I/O completion object has the notification mode FILE_SKIP_COMPLETION_PORT_ON_SUCCESS. The file handle will not notify the I/O completion port and the associated I/O callback function will not be called. </li>
</ul>
To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/499190de-54e8-4be6-909b-04505bcb0aa6">CloseThreadpoolIo</a>



<a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a>



<a href="https://msdn.microsoft.com/5a817d6f-a8e6-4aaa-b560-0128eacb98b1">StartThreadpoolIo</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/68dc640d-8678-441d-88bd-01284d98a251">WaitForThreadpoolIoCallbacks</a>
 

 

