---
UID: NF:processthreadsapi.QueryProtectedPolicy
title: QueryProtectedPolicy function
author: windows-sdk-content
description: Queries the value associated with a protected policy.
old-location: base\queryprotectedpolicy.htm
old-project: procthread
ms.assetid: A9B37117-DE6A-426C-B554-2178247FD4C8
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: QueryProtectedPolicy, QueryProtectedPolicy function, base.getprotectedpolicy, base.queryprotectedpolicy, processthreadsapi/QueryProtectedPolicy
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
 - API-Ms-Win-Core-ProcessThreads-L1-1-2.dll
 - API-Ms-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - QueryProtectedPolicy
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# QueryProtectedPolicy function


## -description


Queries the value associated with a protected policy.


## -parameters




### -param PolicyGuid [in]

	The globally-unique identifier of the policy to query.


### -param PolicyValue [out]

	Receives the value that the supplied policy is set to.


## -returns



True if the function succeeds; otherwise, false.




## -remarks



Protected policies are process-wide configuration settings that are stored in read-only memory. This is intended to help protect the policy from being corrupted or altered in an unintended way while an application is executing.

To compile an application that calls this function, define _WIN32_WINNT as 0x0603 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers.</a>


This function became available in Windows 8.1 and  Windows Server 2012 R2 update 3 (the November 2014 update).



