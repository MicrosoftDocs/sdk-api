---
UID: NF:processthreadsapi.SetProtectedPolicy
title: SetProtectedPolicy function
author: windows-sdk-content
description: Sets a protected policy.
old-location: base\setprotectedpolicy.htm
old-project: procthread
ms.assetid: 36975287-20F0-477B-870F-EA0AC40B39E3
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: SetProtectedPolicy, SetProtectedPolicy function, base.setprotectedpolicy, processthreadsapi/SetProtectedPolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: PROCESS_MEMORY_EXHAUSTION_TYPE, *PPROCESS_MEMORY_EXHAUSTION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Processthreads-L1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SetProtectedPolicy
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# SetProtectedPolicy function


## -description


Sets a protected policy. This function is for use primarily by Windows, and not designed for external use.


## -parameters




### -param PolicyGuid [in]

	The globally-unique identifier of the policy to set.


### -param PolicyValue [in]

	The value to set the policy to.


### -param OldPolicyValue [out]

	Optionally receives the original value that was associated with the supplied policy.


## -returns



	True if the function succeeds; otherwise, false. To retrieve error values for this function, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Protected policies are process-wide configuration settings that are stored in read-only memory. This is intended to help protect the policy from being corrupted or altered in an unintended way while an application is executing. Protected policies are primarily a construct internal to Windows.

To compile an application that calls this function, define _WIN32_WINNT as 0x0603 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers.</a>


This function became available in update 3 (the November 2014 update) for Windows 8.1 and  Windows Server 2012 R2.



