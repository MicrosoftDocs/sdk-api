---
UID: NF:securitybaseapi.ImpersonateSelf
title: ImpersonateSelf function
author: windows-sdk-content
description: Obtains an access token that impersonates the security context of the calling process. The token is assigned to the calling thread.
old-location: security\impersonateself.htm
tech.root: SecAuthZ
ms.assetid: f909e3a7-6c7f-4c05-aa2e-e637113804c9
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: ImpersonateSelf, ImpersonateSelf function [Security], _win32_impersonateself, security.impersonateself, securitybaseapi/ImpersonateSelf
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
 - ImpersonateSelf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImpersonateSelf function


## -description


The <b>ImpersonateSelf</b> function obtains an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> that impersonates the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> of the calling <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">process</a>. The token is assigned to the calling thread.


## -parameters




### -param ImpersonationLevel [in]

Specifies a 
<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a> enumerated type that supplies the impersonation level of the new token.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>ImpersonateSelf</b> function is used for tasks such as enabling a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">privilege</a> for a single thread rather than for the entire process or for changing the default <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) for a single thread.

The server can call the 
<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a> function when the impersonation is complete.

For this function to succeed, the DACL protecting the process token must grant the TOKEN_DUPLICATE right to itself.




## -see-also




<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>



<a href="https://msdn.microsoft.com/63fc90ac-536a-4d9b-ba0d-19dc0cc09e6b">ImpersonateNamedPipeClient</a>



<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a>



<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a>
 

 

