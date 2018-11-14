---
UID: NF:processthreadsapi.SetThreadToken
title: SetThreadToken function
author: windows-sdk-content
description: Assigns an impersonation token to a thread. The function can also cause a thread to stop using an impersonation token.
old-location: security\setthreadtoken.htm
tech.root: secauthz
ms.assetid: ba1a4fce-b3cc-423d-b213-5dfca3dea708
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: SetThreadToken, SetThreadToken function [Security], _win32_setthreadtoken, processthreadsapi/SetThreadToken, security.setthreadtoken
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SetThreadToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetThreadToken
: 
---

# SetThreadToken function


## -description


The <b>SetThreadToken</b> function assigns an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> to a thread. The function can also cause a thread to stop using an impersonation token.


## -parameters




### -param Thread [in, optional]

A pointer to a handle to the thread to which the function assigns the impersonation token. 




If <i>Thread</i> is <b>NULL</b>, the function assigns the impersonation token to the calling thread.


### -param Token [in, optional]

A handle to the impersonation token to assign to the thread. This handle must have been opened with TOKEN_IMPERSONATE access rights. For more information, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>. 




If <i>Token</i> is <b>NULL</b>, the function causes the thread to stop using an impersonation token. 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When using the <b>SetThreadToken</b> function to impersonate, you must have the impersonate  privileges and make sure that the <b>SetThreadToken</b> function succeeds before calling the <a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>
 

 

