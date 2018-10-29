---
UID: NF:threadpoolapiset.StartThreadpoolIo
title: StartThreadpoolIo function
author: windows-sdk-content
description: Notifies the thread pool that I/O operations may possibly begin for the specified I/O completion object. A worker thread calls the I/O completion object's callback function after the operation completes on the file handle bound to this object.
old-location: base\startthreadpoolio.htm
tech.root: ProcThread
ms.assetid: 5a817d6f-a8e6-4aaa-b560-0128eacb98b1
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: StartThreadpoolIo, StartThreadpoolIo function, base.startthreadpoolio, threadpoolapiset/StartThreadpoolIo, winbase/StartThreadpoolIo
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
 - StartThreadpoolIo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StartThreadpoolIo function


## -description


Notifies the thread pool that I/O operations may possibly begin for the specified I/O completion object. A worker thread calls the I/O completion object's callback function after the operation completes on the file handle bound to this object.


## -parameters




### -param pio [in, out]

A <b>TP_IO</b> structure that defines the I/O completion object. The <a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



You must call this function before initiating each asynchronous I/O operation on the file handle bound to the I/O completion object. Failure to do so will cause the thread pool to ignore an I/O operation when it completes and will cause memory corruption.

If the I/O operation fails, call the <a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a> function to cancel this notification.

If the file handle bound to the I/O completion object has the notification mode FILE_SKIP_COMPLETION_PORT_ON_SUCCESS and an asynchronous I/O operation returns immediately with success, the object's I/O completion callback function is not called and threadpool I/O notifications must be canceled. For more information, see  <a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a>.   

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a>



<a href="https://msdn.microsoft.com/499190de-54e8-4be6-909b-04505bcb0aa6">CloseThreadpoolIo</a>



<a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/68dc640d-8678-441d-88bd-01284d98a251">WaitForThreadpoolIoCallbacks</a>
 

 

