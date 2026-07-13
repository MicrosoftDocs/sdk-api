---
UID: NF:processthreadsapi.GetCurrentProcessorNumberEx
title: GetCurrentProcessorNumberEx function (processthreadsapi.h)
description: Retrieves the processor group and number of the logical processor in which the calling thread is running.
helpviewer_keywords: ["GetCurrentProcessorNumberEx","GetCurrentProcessorNumberEx function","base.getcurrentprocessornumberex","processthreadsapi/GetCurrentProcessorNumberEx","winbase/GetCurrentProcessorNumberEx"]
old-location: base\getcurrentprocessornumberex.htm
tech.root: processthreadsapi
ms.assetid: 46c3d3f7-7a82-40d3-8a9e-0f8d0df534f3
ms.date: 12/05/2018
ms.keywords: GetCurrentProcessorNumberEx, GetCurrentProcessorNumberEx function, base.getcurrentprocessornumberex, processthreadsapi/GetCurrentProcessorNumberEx, winbase/GetCurrentProcessorNumberEx
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - GetCurrentProcessorNumberEx
 - processthreadsapi/GetCurrentProcessorNumberEx
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
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - GetCurrentProcessorNumberEx
---

# GetCurrentProcessorNumberEx function


## -description

Retrieves the processor group and number of the logical processor in which the calling thread is running.

## -parameters

### -param ProcNumber [out]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-processor_number">PROCESSOR_NUMBER</a> structure that receives the processor group to which the logical processor is assigned and the number of the logical processor within its group.

## -remarks

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.