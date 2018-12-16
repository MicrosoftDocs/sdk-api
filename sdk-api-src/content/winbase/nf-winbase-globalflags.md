---
UID: NF:winbase.GlobalFlags
title: GlobalFlags function
author: windows-sdk-content
description: Retrieves information about the specified global memory object.
old-location: base\globalflags.htm
tech.root: memory
ms.assetid: 647fc9a2-0522-42ab-ab8b-43c648f27d90
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GlobalFlags, GlobalFlags function, _win32_globalflags, base.globalflags, winbase/GlobalFlags
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - GlobalFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalFlags function


## -description


Retrieves information about the specified global memory object.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. New applications should use the  <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a>. For more information, see Remarks. 
</div><div> </div>

## -parameters




### -param hMem [in]

A handle to the global memory object. This handle is returned by either the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> or 
<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a> function.


## -returns



If the function succeeds, the return value specifies the allocation values and the lock count for the memory object.

If the function fails, the return value is <b>GMEM_INVALID_HANDLE</b>, indicating that the global handle is not valid. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The low-order byte of the low-order word of the return value contains the lock count of the object. To retrieve the lock count from the return value, use the <b>GMEM_LOCKCOUNT</b> mask with the bitwise AND (&amp;) operator. The lock count of memory objects allocated with <b>GMEM_FIXED</b> is always zero.

The high-order byte of the low-order word of the return value indicates the allocation values of the memory object. It can be zero or <b>GMEM_DISCARDED</b>.

The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/af6160ce-ab7a-4198-bca3-dd5d51cacfa5">GlobalDiscard</a>



<a href="https://msdn.microsoft.com/2439b16a-f27d-4e95-bc9e-6f1e563933c9">GlobalReAlloc</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

