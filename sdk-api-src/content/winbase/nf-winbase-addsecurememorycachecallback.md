---
UID: NF:winbase.AddSecureMemoryCacheCallback
title: AddSecureMemoryCacheCallback function
author: windows-sdk-content
description: Registers a callback function to be called when a secured memory range is freed or its protections are changed.
old-location: base\addsecurememorycachecallback.htm
tech.root: memory
ms.assetid: 6c89d6f3-182e-4b10-931c-8d55d603c9dc
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AddSecureMemoryCacheCallback, AddSecureMemoryCacheCallback function, base.addsecurememorycachecallback, winbase/AddSecureMemoryCacheCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
 - kernel32.dll
api_name:
 - AddSecureMemoryCacheCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddSecureMemoryCacheCallback function


## -description


Registers a callback function to be called when a secured memory range is freed or its protections are 
    changed.


## -parameters




### -param pfnCallBack [in]

A pointer to the application-defined 
      <a href="https://msdn.microsoft.com/abde4b6f-7cd8-4a4b-9b00-f035b2c29054">SecureMemoryCacheCallback</a> function to 
      register.


## -returns



If the function succeeds, it registers the callback function and returns 
      <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
      the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



An application that performs I/O directly to a high-performance device typically caches a virtual-to-physical 
    memory mapping for the buffer it uses for the I/O. The device's driver typically secures this memory address range 
    by calling the <a href="https://msdn.microsoft.com/e5c2d5d5-550e-42e5-b86a-f17e361925dc">MmSecureVirtualMemory</a> routine, 
    which prevents the memory range from being freed or its protections  changed until the driver unsecures the 
    memory.

An application can use 
    <b>AddSecureMemoryCacheCallback</b> to register 
    a callback function that will be called when the memory is freed or its protections are changed, so the 
    application can invalidate its cached memory mapping. For more information, see 
    <a href="https://msdn.microsoft.com/abde4b6f-7cd8-4a4b-9b00-f035b2c29054">SecureMemoryCacheCallback</a>.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 
    or later. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/8be6ff04-34c7-4942-a38c-507584c8bbeb">RemoveSecureMemoryCacheCallback</a>



<a href="https://msdn.microsoft.com/abde4b6f-7cd8-4a4b-9b00-f035b2c29054">SecureMemoryCacheCallback</a>
 

 

