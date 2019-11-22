---
UID: NF:processthreadsapi.DeleteProcThreadAttributeList
title: DeleteProcThreadAttributeList function (processthreadsapi.h)

description: Deletes the specified list of attributes for process and thread creation.
old-location: base\deleteprocthreadattributelist.htm
tech.root: ProcThread
ms.assetid: 806326c8-2f1e-4ab8-a6f6-f84763ddc31f

ms.date: 12/05/2018
ms.keywords: DeleteProcThreadAttributeList, DeleteProcThreadAttributeList function, base.deleteprocthreadattributelist, processthreadsapi/DeleteProcThreadAttributeList, winbase/DeleteProcThreadAttributeList
ms.topic: function
f1_keywords: 
 - "processthreadsapi/DeleteProcThreadAttributeList"
dev_langs:
 - c++
req.header: processthreadsapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - DeleteProcThreadAttributeList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteProcThreadAttributeList function


## -description


Deletes the specified list of attributes for process and thread creation.


## -parameters




### -param lpAttributeList [in, out]

The attribute list. This list is created by the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a> function.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
 

 

