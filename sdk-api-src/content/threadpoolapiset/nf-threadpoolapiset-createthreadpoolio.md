---
UID: NF:threadpoolapiset.CreateThreadpoolIo
title: CreateThreadpoolIo function
author: windows-driver-content
description: Creates a new I/O completion object.
old-location: base\createthreadpoolio.htm
old-project: ProcThread
ms.assetid: 621f4747-50fa-4538-bd6a-dbe4dbb05dd1
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: CreateThreadpoolIo, CreateThreadpoolIo function, base.createthreadpoolio, threadpoolapiset/CreateThreadpoolIo, winbase/CreateThreadpoolIo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: threadpoolapiset.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TS_TEXTCHANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-threadpool-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-Core-threadpool-l1-2-0.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	MinKernelBase.dll
api_name:
-	CreateThreadpoolIo
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# CreateThreadpoolIo function


## -description


Creates a new I/O completion object.


## -parameters




### -param fl [in]

The file handle to bind to this I/O completion object.


### -param pfnio [in]

The callback function to be called each time  an overlapped I/O operation completes on the file. For details, see <a href="https://msdn.microsoft.com/50515cec-8359-48a2-a85b-b4382c88107c">IoCompletionCallback</a>.


### -param pv [in, out, optional]

Optional application-defined data to pass to the callback function.


### -param pcbe [in, optional]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the environment in which to execute the callback. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.

If this parameter is NULL, the callback executes in the default callback environment. For more information, see <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>.


## -returns



If the function succeeds, it returns a <b>TP_IO</b> structure that defines the I/O object. Applications do not modify the members of this structure.

If the function fails, it returns NULL. To retrieve extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To begin receiving overlapped I/O completion callbacks, call the <a href="https://msdn.microsoft.com/5a817d6f-a8e6-4aaa-b560-0128eacb98b1">StartThreadpoolIo</a> function.

If the file handle bound to the I/O completion object has the notification mode FILE_SKIP_COMPLETION_PORT_ON_SUCCESS and an asychronous I/O operation returns immediately with success, the I/O completion callback function is not called and threadpool I/O notifications must be canceled. For more information, see <a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a>.   

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/e3af8313-2e09-4c88-8cef-671efd4228c7">CancelThreadpoolIo</a>



<a href="https://msdn.microsoft.com/499190de-54e8-4be6-909b-04505bcb0aa6">CloseThreadpoolIo</a>



<a href="https://msdn.microsoft.com/5a817d6f-a8e6-4aaa-b560-0128eacb98b1">StartThreadpoolIo</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>



<a href="https://msdn.microsoft.com/68dc640d-8678-441d-88bd-01284d98a251">WaitForThreadpoolIoCallbacks</a>
 

 

