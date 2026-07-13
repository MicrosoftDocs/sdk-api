---
UID: NF:processthreadsapi.SetProtectedPolicy
title: SetProtectedPolicy function (processthreadsapi.h)
description: Sets a protected policy.
helpviewer_keywords: ["SetProtectedPolicy","SetProtectedPolicy function","base.setprotectedpolicy","processthreadsapi/SetProtectedPolicy"]
old-location: base\setprotectedpolicy.htm
tech.root: processthreadsapi
ms.assetid: 36975287-20F0-477B-870F-EA0AC40B39E3
ms.date: 12/05/2018
ms.keywords: SetProtectedPolicy, SetProtectedPolicy function, base.setprotectedpolicy, processthreadsapi/SetProtectedPolicy
req.header: processthreadsapi.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetProtectedPolicy
 - processthreadsapi/SetProtectedPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-Processthreads-L1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SetProtectedPolicy
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

	True if the function succeeds; otherwise, false. To retrieve error values for this function, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Protected policies are process-wide configuration settings that are stored in read-only memory. This is intended to help protect the policy from being corrupted or altered in an unintended way while an application is executing. Protected policies are primarily a construct internal to Windows.

To compile an application that calls this function, define _WIN32_WINNT as 0x0603 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers.</a>


This function became available in update 3 (the November 2014 update) for Windows 8.1 and  Windows Server 2012 R2.