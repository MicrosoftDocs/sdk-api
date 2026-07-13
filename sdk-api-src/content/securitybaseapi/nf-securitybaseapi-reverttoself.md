---
UID: NF:securitybaseapi.RevertToSelf
title: RevertToSelf function (securitybaseapi.h)
description: Terminates the impersonation of a client application.
helpviewer_keywords: ["RevertToSelf","RevertToSelf function [Security]","_win32_reverttoself","security.reverttoself","securitybaseapi/RevertToSelf"]
old-location: security\reverttoself.htm
tech.root: security
ms.assetid: e3de77b9-dd27-4f20-b63d-ad2c57ac4283
ms.date: 12/05/2018
ms.keywords: RevertToSelf, RevertToSelf function [Security], _win32_reverttoself, security.reverttoself, securitybaseapi/RevertToSelf
req.header: securitybaseapi.h
req.include-header: Windows.h
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
 - RevertToSelf
 - securitybaseapi/RevertToSelf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - RevertToSelf
---

# RevertToSelf function


## -description

The <b>RevertToSelf</b> function terminates the impersonation of a client application.



## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A <a href="/windows/desktop/SecGloss/p-gly">process</a> should call the <b>RevertToSelf</b> function after finishing any impersonation begun by using the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeimpersonateclient">DdeImpersonateClient</a>, <a href="/windows/desktop/api/dde/nf-dde-impersonateddeclientwindow">ImpersonateDdeClientWindow</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a>, <a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient">ImpersonateNamedPipeClient</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself">ImpersonateSelf</a>, <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateanonymoustoken">ImpersonateAnonymousToken</a> or <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a> function.

An RPC server that used the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a> function to impersonate a client must call the 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself">RpcRevertToSelf</a> or 
<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex">RpcRevertToSelfEx</a> to end the impersonation.

If <b>RevertToSelf</b> fails, your application continues to run in the context of the client, which is not appropriate. You should shut down the process if <b>RevertToSelf</b> fails.


#### Examples

For an example that uses this function, see 
     <a href="/windows/desktop/SecAuthZ/verifying-client-access-with-acls-in-c--">Verifying Client Access with ACLs</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeimpersonateclient">DdeImpersonateClient</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateanonymoustoken">ImpersonateAnonymousToken</a>



<a href="/windows/desktop/api/dde/nf-dde-impersonateddeclientwindow">ImpersonateDdeClientWindow</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient">ImpersonateNamedPipeClient</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself">ImpersonateSelf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient">RpcImpersonateClient</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself">RpcRevertToSelf</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoselfex">RpcRevertToSelfEx</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a>
