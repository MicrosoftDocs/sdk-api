---
UID: NF:processthreadsapi.OpenProcessToken
title: OpenProcessToken function (processthreadsapi.h)
description: Opens the access token associated with a process.helpviewer_keywords: ["OpenProcessToken","OpenProcessToken function [Security]","_win32_openprocesstoken","processthreadsapi/OpenProcessToken","security.openprocesstoken"]
old-location: security\openprocesstoken.htm
tech.root: SecAuthZ
ms.assetid: 1e760ad8-7e46-4748-8c45-36ad8efe936a
ms.date: 12/05/2018
ms.keywords: OpenProcessToken, OpenProcessToken function [Security], _win32_openprocesstoken, processthreadsapi/OpenProcessToken, security.openprocesstoken
f1_keywords:
- processthreadsapi/OpenProcessToken
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenProcessToken function


## -description


The <b>OpenProcessToken</b> function opens the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access token</a> associated with a process.


## -parameters




### -param ProcessHandle [in]

A handle to the process whose access token is opened. The process must have the PROCESS_QUERY_INFORMATION access permission.


### -param DesiredAccess [in]

Specifies an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access mask</a> that specifies the requested types of access to the access token. These requested access types are compared with the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) of the token to determine which accesses are granted or denied. 




For a list of access rights for access tokens, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.


### -param TokenHandle [out]

A pointer to a handle that identifies the newly opened access token when the function returns.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Close the access token handle returned through the <i>TokenHandle</i> parameter by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocesstoken">GetCurrentProcessToken</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadeffectivetoken">GetCurrentThreadEffectiveToken</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadtoken">GetCurrentThreadToken</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>
 

 

