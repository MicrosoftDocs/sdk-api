---
UID: NF:processthreadsapi.OpenProcessToken
title: OpenProcessToken function (processthreadsapi.h)
author: windows-sdk-content
description: Opens the access token associated with a process.
old-location: security\openprocesstoken.htm
tech.root: SecAuthZ
ms.assetid: 1e760ad8-7e46-4748-8c45-36ad8efe936a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: OpenProcessToken, OpenProcessToken function [Security], _win32_openprocesstoken, processthreadsapi/OpenProcessToken, security.openprocesstoken
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Core-Processsecurity-l1-1-0.dll
 - Kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-Processthreads-l1-1-0.dll
 - API-MS-Win-Core-Processthreads-l1-1-1.dll
 - API-MS-Win-Core-Processthreads-l1-1-2.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - OpenProcessToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenProcessToken function


## -description


The <b>OpenProcessToken</b> function opens the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> associated with a process.


## -parameters




### -param ProcessHandle [in]

A handle to the process whose access token is opened. The process must have the PROCESS_QUERY_INFORMATION access permission.


### -param DesiredAccess [in]

Specifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> that specifies the requested types of access to the access token. These requested access types are compared with the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) of the token to determine which accesses are granted or denied. 




For a list of access rights for access tokens, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -param TokenHandle [out]

A pointer to a handle that identifies the newly opened access token when the function returns.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Close the access token handle returned through the <i>TokenHandle</i> parameter by calling 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a>



<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/9DD1781A-4C77-4E22-9FCF-579FC90F3028">GetCurrentProcessToken</a>



<a href="https://msdn.microsoft.com/794E9086-17E7-4520-AB30-63DF00FF7AA4">GetCurrentThreadEffectiveToken</a>



<a href="https://msdn.microsoft.com/D56FE64F-CFE0-4BE4-BBDA-DF0B79E3E86F">GetCurrentThreadToken</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>
 

 

