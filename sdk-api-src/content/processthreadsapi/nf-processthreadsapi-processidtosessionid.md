---
UID: NF:processthreadsapi.ProcessIdToSessionId
title: ProcessIdToSessionId function (processthreadsapi.h)
author: windows-sdk-content
description: Retrieves the Remote Desktop Services session associated with a specified process.
old-location: termserv\processidtosessionid.htm
tech.root: TermServ
ms.assetid: 99a3f047-705c-40bc-8cc2-055257a4f2b3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ProcessIdToSessionId, ProcessIdToSessionId function [Remote Desktop Services], _win32_processidtosessionid, processthreadsapi/ProcessIdToSessionId, termserv.processidtosessionid
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - API-MS-Win-Downlevel-Kernel32-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - ProcessIdToSessionId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ProcessIdToSessionId function


## -description


Retrieves the Remote Desktop Services session 
    associated with a specified process.


## -parameters




### -param dwProcessId [in]

Specifies a process identifier. Use the 
      <a href="https://msdn.microsoft.com/a442e147-0db0-4911-94de-91728a4b277a">GetCurrentProcessId</a> function to retrieve the 
      process identifier for the current process.


### -param pSessionId [out]

Pointer to a variable that receives the identifier of the Remote Desktop Services session under which the 
      specified process is running. To retrieve the identifier of the session currently attached to the console, use 
  the <a href="https://msdn.microsoft.com/9aa43cfa-9518-428b-95a1-004fa23df90b">WTSGetActiveConsoleSessionId</a> 
  function.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Callers must hold the <b>PROCESS_QUERY_INFORMATION</b> access right for the specified 
    process. For more information, see 
  <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.




## -see-also




<a href="https://msdn.microsoft.com/4ab07a72-404d-459b-b061-b3b06b5db37e">OSVERSIONINFOEX</a>



<a href="https://msdn.microsoft.com/d52345a4-0408-4ea9-ba71-349910143752">WTSQuerySessionInformation</a>
 

 

