---
UID: NF:processthreadsapi.QueryProtectedPolicy
title: QueryProtectedPolicy function (processthreadsapi.h)
description: Queries the value associated with a protected policy.
helpviewer_keywords: ["QueryProtectedPolicy","QueryProtectedPolicy function","base.getprotectedpolicy","base.queryprotectedpolicy","processthreadsapi/QueryProtectedPolicy"]
old-location: base\queryprotectedpolicy.htm
tech.root: processthreadsapi
ms.assetid: A9B37117-DE6A-426C-B554-2178247FD4C8
ms.date: 12/05/2018
ms.keywords: QueryProtectedPolicy, QueryProtectedPolicy function, base.getprotectedpolicy, base.queryprotectedpolicy, processthreadsapi/QueryProtectedPolicy
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
 - QueryProtectedPolicy
 - processthreadsapi/QueryProtectedPolicy
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
 - API-Ms-Win-Core-ProcessThreads-L1-1-2.dll
 - API-Ms-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - QueryProtectedPolicy
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

To compile an application that calls this function, define _WIN32_WINNT as 0x0603 or later. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers.</a>


This function became available in Windows 8.1 and  Windows Server 2012 R2 update 3 (the November 2014 update).