---
UID: NF:fibersapi.FlsGetValue
title: FlsGetValue function
author: windows-sdk-content
description: Retrieves the value in the calling fiber's fiber local storage (FLS) slot for the specified FLS index. Each fiber has its own slot for each FLS index.
old-location: base\flsgetvalue.htm
tech.root: ProcThread
ms.assetid: 5d5a1fe6-10ed-42c5-87db-b24eef6f174c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlsGetValue, FlsGetValue function, _win32_flsgetvalue, base.flsgetvalue, fibersapi/FlsGetValue, winbase/FlsGetValue
ms.topic: function
req.header: fibersapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-fibers-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-fibers-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FlsGetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FlsGetValue function


## -description


Retrieves the value in the calling fiber's fiber local storage (FLS) slot for the specified FLS index. Each fiber has its own slot for each FLS index.


## -parameters




### -param dwFlsIndex [in]

The FLS index that was allocated by the 
<a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a> function.


## -returns



If the function succeeds, the return value is the value stored in the calling fiber's FLS slot associated with the specified index.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



FLS indexes are typically allocated by the 
<a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a> function during process or DLL initialization. After an FLS index is allocated, each fiber of the process can use it to access its own FLS slot for that index. A fiber specifies an FLS index in a call to 
<a href="https://msdn.microsoft.com/f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad">FlsSetValue</a> to store a value in its slot. The thread specifies the same index in a subsequent call to 
<b>FlsSetValue</b> to retrieve the stored value.




## -see-also




<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a>



<a href="https://msdn.microsoft.com/f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad">FlsSetValue</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

