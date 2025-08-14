---
UID: NF:processthreadsapi.InitializeProcThreadAttributeList
title: InitializeProcThreadAttributeList function (processthreadsapi.h)
description: Initializes the specified list of attributes for process and thread creation.
helpviewer_keywords: ["InitializeProcThreadAttributeList","InitializeProcThreadAttributeList function","base.initializeprocthreadattributelist","processthreadsapi/InitializeProcThreadAttributeList","winbase/InitializeProcThreadAttributeList"]
old-location: base\initializeprocthreadattributelist.htm
tech.root: processthreadsapi
ms.assetid: 58ce70a1-5b73-429f-a062-bacd9b9c5bc8
ms.date: 12/05/2018
ms.keywords: InitializeProcThreadAttributeList, InitializeProcThreadAttributeList function, base.initializeprocthreadattributelist, processthreadsapi/InitializeProcThreadAttributeList, winbase/InitializeProcThreadAttributeList
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - InitializeProcThreadAttributeList
 - processthreadsapi/InitializeProcThreadAttributeList
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
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - InitializeProcThreadAttributeList
---

# InitializeProcThreadAttributeList function


## -description

Initializes the specified list of attributes for process and thread creation.

## -parameters

### -param lpAttributeList [out, optional]

The attribute list. This parameter can be NULL to determine the buffer size required to support the specified number of attributes.

### -param dwAttributeCount [in]

The count of attributes to be added to the list.

### -param dwFlags

This parameter is reserved and must be zero.

### -param lpSize [in, out]

If <i>lpAttributeList</i> is not NULL, this parameter specifies the size in bytes of the <i>lpAttributeList</i> buffer on input. On output, this parameter receives the size in bytes of the initialized attribute list. 

If <i>lpAttributeList</i> is NULL, this parameter receives the required buffer size in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

First, call this function with the <i>dwAttributeCount</i> parameter set to the maximum number of attributes you will be using and the <i>lpAttributeList</i> to NULL. The function returns the required buffer size in bytes in the <i>lpSize</i> parameter. 

<div class="alert"><b>Note</b>  This initial call will return an error by design. This is expected behavior.</div>
<div> </div>
Allocate enough space for the data in the <i>lpAttributeList</i> buffer and call the function again to initialize the buffer.

To add attributes to the list, call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">UpdateProcThreadAttribute</a> function. To specify these attributes when creating a process, specify EXTENDED_STARTUPINFO_PRESENT in the <i>dwCreationFlag</i> parameter and a <a href="/windows/desktop/api/winbase/ns-winbase-startupinfoexa">STARTUPINFOEX</a> structure in the <i>lpStartupInfo</i> parameter. Note that you can specify the same <b>STARTUPINFOEX</b> structure to multiple child processes.

When you have finished using the list, call the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist">DeleteProcThreadAttributeList</a> function.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-deleteprocthreadattributelist">DeleteProcThreadAttributeList</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute">UpdateProcThreadAttribute</a>