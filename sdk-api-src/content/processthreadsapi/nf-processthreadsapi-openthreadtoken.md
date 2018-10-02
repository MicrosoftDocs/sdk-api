---
UID: NF:processthreadsapi.OpenThreadToken
title: OpenThreadToken function
author: windows-sdk-content
description: Opens the access token associated with a thread.
old-location: security\openthreadtoken.htm
tech.root: SecAuthZ
ms.assetid: 5003f0c4-41e9-4a14-b6a9-4f259c4af08b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OpenThreadToken, OpenThreadToken function [Security], _win32_openthreadtoken, processthreadsapi/OpenThreadToken, security.openthreadtoken
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - OpenThreadToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenThreadToken function


## -description


The <b>OpenThreadToken</b> function opens the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> associated with a thread.


## -parameters




### -param ThreadHandle [in]

A handle to the thread whose access token is opened.


### -param DesiredAccess [in]

Specifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> that specifies the requested types of access to the access token. These requested access types are reconciled against the token's <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) to determine which accesses are granted or denied. 




For a list of access rights for access tokens, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -param OpenAsSelf [in]

TRUE if the access check is to be made against the  process-level <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.

<b>FALSE</b> if the access check is to be made against the current security context of the thread calling the <b>OpenThreadToken</b> function.

The <i>OpenAsSelf</i> parameter allows the caller of this function to open the access token of a specified thread when the caller is impersonating a token at <b>SecurityIdentification</b> level. Without this parameter, the calling thread cannot open the access token on the specified thread because it is impossible to open executive-level objects by using the <b>SecurityIdentification</b> impersonation level.


### -param TokenHandle [out]

A pointer to a variable that receives the handle to the newly opened access token.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. If the token has the anonymous impersonation level, the token will not be opened and <b>OpenThreadToken</b> sets  ERROR_CANT_OPEN_ANONYMOUS as the error.




## -remarks



Tokens with the anonymous impersonation level cannot be opened.

Close the access token handle returned through the <i>TokenHandle</i> parameter by calling 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a>



<a href="https://msdn.microsoft.com/839c4b58-4c61-4f72-8337-1e3dfa267ee5">AdjustTokenGroups</a>



<a href="https://msdn.microsoft.com/8e3f70cd-814e-4aab-8f48-0ca482beef2e">AdjustTokenPrivileges</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/D56FE64F-CFE0-4BE4-BBDA-DF0B79E3E86F">GetCurrentThreadToken</a>



<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>



<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a>



<a href="https://msdn.microsoft.com/ba1a4fce-b3cc-423d-b213-5dfca3dea708">SetThreadToken</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>
 

 

