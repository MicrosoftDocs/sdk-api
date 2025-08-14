---
UID: NF:processthreadsapi.IsProcessCritical
title: IsProcessCritical function (processthreadsapi.h)
description: Determines whether the specified process is considered critical.
helpviewer_keywords: ["IsProcessCritical","IsProcessCritical function","base.isprocesscritical","processthreadsapi/IsProcessCritical"]
old-location: base\isprocesscritical.htm
tech.root: processthreadsapi
ms.assetid: A5ED8672-B4C3-4A31-8B3F-A181628219A4
ms.date: 09/24/2020
ms.keywords: IsProcessCritical, IsProcessCritical function, base.isprocesscritical, processthreadsapi/IsProcessCritical
req.header: processthreadsapi.h
req.include-header: 
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
req.dll: kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsProcessCritical
 - processthreadsapi/IsProcessCritical
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
 - kernel32.dll
 - API-MS-Win-Core-Processthreads-l1-1-2.dll
 - Kernel32.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - IsProcessCritical
---

# IsProcessCritical function


## -description

Determines whether the specified process is considered critical.

## -parameters

### -param hProcess [in]

A handle to the process to query. The process must have been          opened with <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access.

### -param Critical [out]

A pointer to the <b>BOOL</b> value this function will use to indicate whether the process          is considered critical.

## -returns

This routine returns FALSE on failure. Any other value indicates success.      Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to query for the specific error reason on failure.

## -see-also

<a href="/windows/desktop/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a>