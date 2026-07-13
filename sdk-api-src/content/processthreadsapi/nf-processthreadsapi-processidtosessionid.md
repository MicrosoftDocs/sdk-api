---
UID: NF:processthreadsapi.ProcessIdToSessionId
title: ProcessIdToSessionId function (processthreadsapi.h)
description: Retrieves the Remote Desktop Services session associated with a specified process.
helpviewer_keywords: ["ProcessIdToSessionId","ProcessIdToSessionId function [Remote Desktop Services]","_win32_processidtosessionid","processthreadsapi/ProcessIdToSessionId","termserv.processidtosessionid"]
old-location: termserv\processidtosessionid.htm
tech.root: processthreadsapi
ms.assetid: 99a3f047-705c-40bc-8cc2-055257a4f2b3
ms.date: 12/05/2018
ms.keywords: ProcessIdToSessionId, ProcessIdToSessionId function [Remote Desktop Services], _win32_processidtosessionid, processthreadsapi/ProcessIdToSessionId, termserv.processidtosessionid
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - ProcessIdToSessionId
 - processthreadsapi/ProcessIdToSessionId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
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
---

# ProcessIdToSessionId function


## -description

Retrieves the Remote Desktop Services session 
    associated with a specified process.

## -parameters

### -param dwProcessId [in]

Specifies a process identifier. Use the 
      <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid">GetCurrentProcessId</a> function to retrieve the 
      process identifier for the current process.

### -param pSessionId [out]

Pointer to a variable that receives the identifier of the Remote Desktop Services session under which the 
      specified process is running. To retrieve the identifier of the session currently attached to the console, use 
  the <a href="/windows/desktop/api/winbase/nf-winbase-wtsgetactiveconsolesessionid">WTSGetActiveConsoleSessionId</a> 
  function.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Callers must hold the <b>PROCESS_QUERY_INFORMATION</b> access right for the specified 
    process. For more information, see 
  <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-osversioninfoexa">OSVERSIONINFOEX</a>



<a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a>