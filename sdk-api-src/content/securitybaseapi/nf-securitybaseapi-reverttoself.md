---
UID: NF:securitybaseapi.RevertToSelf
title: RevertToSelf function
author: windows-sdk-content
description: Terminates the impersonation of a client application.
old-location: security\reverttoself.htm
tech.root: SecAuthZ
ms.assetid: e3de77b9-dd27-4f20-b63d-ad2c57ac4283
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: RevertToSelf, RevertToSelf function [Security], _win32_reverttoself, security.reverttoself, securitybaseapi/RevertToSelf
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RevertToSelf function


## -description


The <b>RevertToSelf</b> function terminates the impersonation of a client application.


## -parameters






## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a> should call the <b>RevertToSelf</b> function after finishing any impersonation begun by using the <a href="https://msdn.microsoft.com/en-us/library/ms648756(v=VS.85).aspx">DdeImpersonateClient</a>, <a href="https://msdn.microsoft.com/en-us/library/ms649005(v=VS.85).aspx">ImpersonateDdeClientWindow</a>, <a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a>, <a href="https://msdn.microsoft.com/63fc90ac-536a-4d9b-ba0d-19dc0cc09e6b">ImpersonateNamedPipeClient</a>, <a href="https://msdn.microsoft.com/f909e3a7-6c7f-4c05-aa2e-e637113804c9">ImpersonateSelf</a>, <a href="https://msdn.microsoft.com/98d1072e-f569-4c8c-9254-fa558054c7ec">ImpersonateAnonymousToken</a> or <a href="https://msdn.microsoft.com/ba1a4fce-b3cc-423d-b213-5dfca3dea708">SetThreadToken</a> function.

An RPC server that used the 
<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a> function to impersonate a client must call the 
<a href="https://msdn.microsoft.com/07bbf6fa-f1df-4d9c-ae67-e79e2ccc12c8">RpcRevertToSelf</a> or 
<a href="https://msdn.microsoft.com/8860cee2-7e53-4a07-a379-fd00f3d01def">RpcRevertToSelfEx</a> to end the impersonation.

If <b>RevertToSelf</b> fails, your application continues to run in the context of the client, which is not appropriate. You should shut down the process if <b>RevertToSelf</b> fails.


#### Examples

For an example that uses this function, see 
     <a href="https://msdn.microsoft.com/de21968e-4590-4798-9152-43204d55521f">Verifying Client Access with ACLs</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648756(v=VS.85).aspx">DdeImpersonateClient</a>



<a href="https://msdn.microsoft.com/98d1072e-f569-4c8c-9254-fa558054c7ec">ImpersonateAnonymousToken</a>



<a href="https://msdn.microsoft.com/en-us/library/ms649005(v=VS.85).aspx">ImpersonateDdeClientWindow</a>



<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a>



<a href="https://msdn.microsoft.com/63fc90ac-536a-4d9b-ba0d-19dc0cc09e6b">ImpersonateNamedPipeClient</a>



<a href="https://msdn.microsoft.com/f909e3a7-6c7f-4c05-aa2e-e637113804c9">ImpersonateSelf</a>



<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>



<a href="https://msdn.microsoft.com/07bbf6fa-f1df-4d9c-ae67-e79e2ccc12c8">RpcRevertToSelf</a>



<a href="https://msdn.microsoft.com/8860cee2-7e53-4a07-a379-fd00f3d01def">RpcRevertToSelfEx</a>



<a href="https://msdn.microsoft.com/ba1a4fce-b3cc-423d-b213-5dfca3dea708">SetThreadToken</a>
 

 

