---
UID: NF:securitybaseapi.ImpersonateAnonymousToken
title: ImpersonateAnonymousToken function
author: windows-sdk-content
description: Enables the specified thread to impersonate the system's anonymous logon token.
old-location: security\impersonateanonymoustoken.htm
tech.root: SecAuthZ
ms.assetid: 98d1072e-f569-4c8c-9254-fa558054c7ec
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ImpersonateAnonymousToken, ImpersonateAnonymousToken function [Security], _win32_impersonateanonymoustoken, security.impersonateanonymoustoken, securitybaseapi/ImpersonateAnonymousToken
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - ImpersonateAnonymousToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ImpersonateAnonymousToken
: 
---

# ImpersonateAnonymousToken function


## -description


The <b>ImpersonateAnonymousToken</b> function enables the specified thread to impersonate the system's anonymous logon token. To ensure that a token matches the operating system's concept of anonymous access, this function should be called before attempting network access to generate an anonymous token on the remote server.


## -parameters




### -param ThreadHandle [in]

A handle to the thread to impersonate the system's anonymous logon token.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

An error of ACCESS_DENIED may indicate that the token is for a restricted process. Use OpenProcessToken and IsTokenRestricted to check if the process is restricted.




## -remarks



Anonymous tokens do not include the Everyone Group SID unless the system default has been overridden by setting the HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa\EveryoneIncludesAnonymous registry value to DWORD=1.

To cancel the impersonation call 
<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a>
 

 

