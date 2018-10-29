---
UID: NF:winbase.LocalHandle
title: LocalHandle function
author: windows-sdk-content
description: Retrieves the handle associated with the specified pointer to a local memory object.
old-location: base\localhandle.htm
tech.root: Memory
ms.assetid: 2b252f8b-d0a3-4d7f-9e2e-cb80c1512935
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: LocalHandle, LocalHandle function, _win32_localhandle, base.localhandle, winbase/LocalHandle
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
api_name:
 - LocalHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LocalHandle function


## -description


Retrieves the handle associated with the specified pointer to a local memory object.
<div class="alert"><b>Note</b>  The local functions have greater overhead and provide fewer features than other memory management functions. New applications should use the <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> unless documentation states that a local function should be used. For more information, see <a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>.</div><div> </div>

## -parameters




### -param pMem [in]

A pointer to the first byte of the local memory object. This pointer is returned by the 
<a href="https://msdn.microsoft.com/a9432e28-9fbd-4a7e-8dce-fad3da04804a">LocalLock</a> function.


## -returns



If the function succeeds, the return value is a handle to the specified local memory object.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When the 
<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> function allocates a local memory object with <b>LMEM_MOVEABLE</b>, it returns a handle to the object. The 
<a href="https://msdn.microsoft.com/a9432e28-9fbd-4a7e-8dce-fad3da04804a">LocalLock</a> function converts this handle into a pointer to the object's memory block, and 
<b>LocalHandle</b> converts the pointer back into a handle.




## -see-also




<a href="https://msdn.microsoft.com/97707ce7-4c65-4d0e-ba69-47fdaee73a9b">Global and Local Functions</a>



<a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a>



<a href="https://msdn.microsoft.com/a9432e28-9fbd-4a7e-8dce-fad3da04804a">LocalLock</a>



<a href="https://msdn.microsoft.com/5a2a7a62-0bda-4a0d-93d2-25b4898871fd">Memory
    Management Functions</a>
 

 

