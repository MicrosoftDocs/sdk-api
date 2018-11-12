---
UID: NF:winbase.GlobalSize
title: GlobalSize function
author: windows-sdk-content
description: Retrieves the current size of the specified global memory object, in bytes.
old-location: base\globalsize.htm
tech.root: memory
ms.assetid: 9fd01460-d6fc-41f4-9e0c-209a3d1844c1
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GlobalSize, GlobalSize function, _win32_globalsize, base.globalsize, winbase/GlobalSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-Heap-Obsolete-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - GlobalSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalSize function


## -description


Retrieves the current size of the specified global memory object, in bytes.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.
</div><div> </div>

## -parameters




### -param hMem [in]

A handle to the global memory object. This handle is returned by either the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> or 
<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function.


## -returns



If the function succeeds, the return value is the size of the specified global memory object, in bytes.

If the specified handle is not valid or if the object has been discarded, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The size of a memory block may be larger than the size requested when the memory was allocated.

To verify that the specified object's memory block has not been discarded, use the 
<a href="https://msdn.microsoft.com/647fc9a2-0522-42ab-ab8b-43c648f27d90">GlobalFlags</a> function before calling 
<b>GlobalSize</b>.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/647fc9a2-0522-42ab-ab8b-43c648f27d90">GlobalFlags</a>



<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
		  Management Functions</a>
 

 

