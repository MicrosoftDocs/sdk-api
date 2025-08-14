---
UID: NF:namedpipeapi.ImpersonateNamedPipeClient
title: ImpersonateNamedPipeClient function (namedpipeapi.h)
description: Impersonates a named-pipe client application.
helpviewer_keywords: ["ImpersonateNamedPipeClient","ImpersonateNamedPipeClient function [Security]","_win32_impersonatenamedpipeclient","namedpipeapi/ImpersonateNamedPipeClient","security.impersonatenamedpipeclient"]
old-location: security\impersonatenamedpipeclient.htm
tech.root: security
ms.assetid: 63fc90ac-536a-4d9b-ba0d-19dc0cc09e6b
ms.date: 12/05/2018
ms.keywords: ImpersonateNamedPipeClient, ImpersonateNamedPipeClient function [Security], _win32_impersonatenamedpipeclient, namedpipeapi/ImpersonateNamedPipeClient, security.impersonatenamedpipeclient
req.header: namedpipeapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImpersonateNamedPipeClient
 - namedpipeapi/ImpersonateNamedPipeClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-Core-NamedPipe-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-NamedPipe-l1-2-0.dll
 - API-MS-Win-Core-Processsecurity-l1-1-0.dll
 - Kernel32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-NamedPipe-l1-2-1.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
 - ImpersonateNamedPipeClient
---

# ImpersonateNamedPipeClient function


## -description

The <b>ImpersonateNamedPipeClient</b> function impersonates a named-pipe client application.

## -parameters

### -param hNamedPipe [in]

A handle to a named pipe.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>ImpersonateNamedPipeClient</b> function allows the server end of a named pipe to impersonate the client end. When this function is called, the named-pipe file system changes the thread of the calling <a href="/windows/win32/SecGloss/p-gly">process</a> to start impersonating the <a href="/windows/win32/SecGloss/s-gly">security context</a> of the last message read from the pipe. Only the server end of the pipe can call this function.

The server can call the 
<a href="/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a> function when the impersonation is complete.

<div class="alert"><b>Important</b>  If the <b>ImpersonateNamedPipeClient</b> function fails, the client is not impersonated, and all subsequent client requests are made in the security context of the process that called the function. If the calling process is running as a privileged account, it can perform actions that the client would not be allowed to perform. To avoid security risks, the calling process should always check the return value. If the return value indicates that the function call failed, no client requests should be executed.</div>
<div> </div>
All impersonate functions, including <b>ImpersonateNamedPipeClient</b> allow the requested impersonation if one of the following is true: 



<ul>
<li>The requested impersonation level of the token is less than <b>SecurityImpersonation</b>, such as <b>SecurityIdentification</b> or <b>SecurityAnonymous</b>.</li>
<li>The caller has the <b>SeImpersonatePrivilege</b> privilege.</li>
<li>A process (or another process in the caller's logon session) created the token using explicit credentials through <a href="/windows/win32/api/winbase/nf-winbase-logonusera">LogonUser</a> or <a href="/windows/win32/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function.</li>
<li>The authenticated identity is same as the caller.</li>
</ul>
<b>Windows XP with SP1 and earlier:  </b>The <b>SeImpersonatePrivilege</b> privilege is not supported.


#### Examples

For an example that uses this function, see 
     <a href="/windows/win32/SecAuthZ/verifying-client-access-with-acls-in-c--">Verifying Client Access with ACLs</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/secauthz/authorization-functions">Authorization functions</a>



<a href="/windows/win32/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/win32/api/ddeml/nf-ddeml-ddeimpersonateclient">DdeImpersonateClient</a>



<a href="/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>



<a href="/windows/win32/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>

