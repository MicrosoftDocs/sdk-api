---
UID: NF:processthreadsapi.DeleteProcThreadAttributeList
title: DeleteProcThreadAttributeList function
author: windows-sdk-content
description: Deletes the specified list of attributes for process and thread creation.
old-location: base\deleteprocthreadattributelist.htm
tech.root: procthread
ms.assetid: 806326c8-2f1e-4ab8-a6f6-f84763ddc31f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteProcThreadAttributeList, DeleteProcThreadAttributeList function, base.deleteprocthreadattributelist, processthreadsapi/DeleteProcThreadAttributeList, winbase/DeleteProcThreadAttributeList
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteProcThreadAttributeList function


## -description


Deletes the specified list of attributes for process and thread creation.


## -parameters




### -param lpAttributeList [in, out]

The attribute list. This list is created by the <a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a> function.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

