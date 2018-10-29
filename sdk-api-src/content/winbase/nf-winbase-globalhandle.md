---
UID: NF:winbase.GlobalHandle
title: GlobalHandle function
author: windows-sdk-content
description: Retrieves the handle associated with the specified pointer to a global memory block.
old-location: base\globalhandle.htm
tech.root: Memory
ms.assetid: 18ed3446-060a-4874-8187-5c54fb936da9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GlobalHandle, GlobalHandle function, _win32_globalhandle, base.globalhandle, winbase/GlobalHandle
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - GlobalHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GlobalHandle function


## -description


Retrieves the handle associated with the specified pointer to a global memory block.
<div class="alert"><b>Note</b>  The global functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a global function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.
</div><div> </div>

## -parameters




### -param pMem [in]

A pointer to the first byte of the global memory block. This pointer is returned by the 
<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a> function.


## -returns



If the function succeeds, the return value is a handle to the specified global memory object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When the 
<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> function allocates a memory object with <b>GMEM_MOVEABLE</b>, it returns a handle to the object. The 
<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a> function converts this handle into a pointer to the memory block, and 
<b>GlobalHandle</b> converts the pointer back into a handle.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a>



<a href="https://msdn.microsoft.com/0d7deac2-c9c4-4adc-8a0a-edfc512a4d6c">GlobalLock</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

