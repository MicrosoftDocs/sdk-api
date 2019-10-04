---
UID: NF:threadpoolapiset.SetThreadpoolStackInformation
title: SetThreadpoolStackInformation function (threadpoolapiset.h)
author: windows-sdk-content
description: Sets the stack reserve and commit sizes for new threads in the specified thread pool. Stack reserve and commit sizes for existing threads are not changed.
old-location: base\setthreadpoolstackinformation.htm
tech.root: ProcThread
ms.assetid: dbed0a95-30d8-4e63-b141-743401103c53
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetThreadpoolStackInformation, SetThreadpoolStackInformation function, base.setthreadpoolstackinformation, threadpoolapiset/SetThreadpoolStackInformation, winbase/SetThreadpoolStackInformation
ms.topic: function
f1_keywords: 
 - "threadpoolapiset/SetThreadpoolStackInformation"
dev_langs:
 - c++
req.header: threadpoolapiset.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - kernel32.dll
 - API-MS-Win-Core-threadpool-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-threadpool-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetThreadpoolStackInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetThreadpoolStackInformation function


## -description


Sets the stack reserve and commit sizes for new threads in the specified thread pool. Stack reserve and commit sizes for existing threads are not changed.


## -parameters




### -param ptpp [in, out]

A <b>TP_POOL</b> structure that specifies the thread pool. The <a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-createthreadpool">CreateThreadpool</a> function returns this structure.


### -param ptpsi [in]

A <b>TP_POOL_STACK_INFORMATION</b> structure that specifies the stack reserve and commit size for threads in the pool. 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 




## -remarks



To compile an application that uses this function, set _WIN32_WINNT to _WIN32_WINNT_WIN7. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/threadpoolapiset/nf-threadpoolapiset-querythreadpoolstackinformation">QueryThreadpoolStackInformation</a>
 

 

