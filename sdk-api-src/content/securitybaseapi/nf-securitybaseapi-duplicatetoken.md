---
UID: NF:securitybaseapi.DuplicateToken
title: DuplicateToken function
author: windows-sdk-content
description: Creates a new access token that duplicates one already in existence.
old-location: security\duplicatetoken.htm
tech.root: secauthz
ms.assetid: 796ec60e-fcae-48a9-b471-de3dce831306
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: DuplicateToken, DuplicateToken function [Security], _win32_duplicatetoken, security.duplicatetoken, securitybaseapi/DuplicateToken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - DuplicateToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DuplicateToken function


## -description


The <b>DuplicateToken</b> function creates a new <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> that duplicates one already in existence.


## -parameters




### -param ExistingTokenHandle [in]

A handle to an access token opened with TOKEN_DUPLICATE access.


### -param ImpersonationLevel [in]

Specifies a 
<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a> enumerated type that supplies the impersonation level of the new token.


### -param DuplicateTokenHandle [out]

A pointer to a variable that receives a handle to the duplicate token. This handle has TOKEN_IMPERSONATE and TOKEN_QUERY access to the new token.

When you have finished using the new token, call the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the token handle.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>DuplicateToken</b> function creates an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>, which you can use in functions such as <a href="https://msdn.microsoft.com/ba1a4fce-b3cc-423d-b213-5dfca3dea708">SetThreadToken</a> and <a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a>. The token created by <b>DuplicateToken</b> cannot be used in the <a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function, which requires a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a>. To create a token that you can pass to <b>CreateProcessAsUser</b>, use the <a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/96b13826-0ac7-4d70-9c21-eeb343f6b823">DuplicateTokenEx</a>



<a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a>



<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a>



<a href="https://msdn.microsoft.com/ba1a4fce-b3cc-423d-b213-5dfca3dea708">SetThreadToken</a>
 

 

