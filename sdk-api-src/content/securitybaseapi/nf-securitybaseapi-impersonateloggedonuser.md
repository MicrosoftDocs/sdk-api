---
UID: NF:securitybaseapi.ImpersonateLoggedOnUser
title: ImpersonateLoggedOnUser function
author: windows-sdk-content
description: Lets the calling thread impersonate the security context of a logged-on user. The user is represented by a token handle.
old-location: security\impersonateloggedonuser.htm
old-project: secauthz
ms.assetid: cf5c31ae-6749-45c2-888f-697060cc8c75
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ImpersonateLoggedOnUser, ImpersonateLoggedOnUser function [Security], _win32_impersonateloggedonuser, security.impersonateloggedonuser, securitybaseapi/ImpersonateLoggedOnUser
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - ImpersonateLoggedOnUser
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# ImpersonateLoggedOnUser function


## -description


The <b>ImpersonateLoggedOnUser</b> function lets the calling thread impersonate the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> of a logged-on user. The user is represented by a token handle.


## -parameters




### -param hToken [in]

A handle to a primary or impersonation <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> that represents a logged-on user. This can be a token handle returned by a call to 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, 
<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, 
<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, 
<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a>, 
<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or 
<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> functions. If <i>hToken</i> is a handle to a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a>, the token must have <b>TOKEN_QUERY</b> and <b>TOKEN_DUPLICATE</b> access. If <i>hToken</i> is a handle to an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>, the token must have <b>TOKEN_QUERY</b> and <b>TOKEN_IMPERSONATE</b> access.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The impersonation lasts until the thread exits or until it calls 
<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a>.

The calling thread does not need to have any particular <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> to call <b>ImpersonateLoggedOnUser</b>.

If the call to <b>ImpersonateLoggedOnUser</b> fails, the client connection is not impersonated and the client request is made in the security context of the process. If the process is running as a highly privileged account, such as LocalSystem, or as a member of an administrative group, the user may be able to perform actions they would otherwise be disallowed. Therefore, it is important to always check the return value of the call, and if it fails, raise an error; do not continue execution of the client request.

All impersonate functions, including <b>ImpersonateLoggedOnUser</b> allow the requested impersonation if one of the following is true: 



<ul>
<li>The requested impersonation level of the token is less than <b>SecurityImpersonation</b>, such as <b>SecurityIdentification</b> or <b>SecurityAnonymous</b>.</li>
<li>The caller has the <b>SeImpersonatePrivilege</b> privilege.</li>
<li>A process (or another process in the caller's logon session) created the token using explicit credentials through <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> or <a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> function.</li>
<li>The authenticated identity is same as the caller.</li>
</ul>
<b>Windows XP with SP1 and earlier:  </b>The <b>SeImpersonatePrivilege</b> privilege is not supported.

For more information about impersonation, see 
<a href="https://msdn.microsoft.com/a3f74372-bdc9-43eb-b72f-7d00a43e78a8">Client Impersonation</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>



<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>



<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a>



<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>



<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>



<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a>
 

 

