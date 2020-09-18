---
UID: NF:winbase.AddSecureMemoryCacheCallback
title: AddSecureMemoryCacheCallback function (winbase.h)
description: Registers a callback function to be called when a secured memory range is freed or its protections are changed.
helpviewer_keywords: ["AddSecureMemoryCacheCallback","AddSecureMemoryCacheCallback function","base.addsecurememorycachecallback","winbase/AddSecureMemoryCacheCallback"]
old-location: base\addsecurememorycachecallback.htm
tech.root: base
ms.assetid: 6c89d6f3-182e-4b10-931c-8d55d603c9dc
ms.date: 12/05/2018
ms.keywords: AddSecureMemoryCacheCallback, AddSecureMemoryCacheCallback function, base.addsecurememorycachecallback, winbase/AddSecureMemoryCacheCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddSecureMemoryCacheCallback
 - winbase/AddSecureMemoryCacheCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
api_name:
 - AddSecureMemoryCacheCallback
---

# AddSecureMemoryCacheCallback function


## -description

Registers a callback function to be called when a secured memory range is freed or its protections are 
    changed.

## -parameters

### -param pfnCallBack [in]

A pointer to the application-defined 
      <a href="/windows/desktop/api/winnt/nc-winnt-psecure_memory_cache_callback">SecureMemoryCacheCallback</a> function to 
      register.

## -returns

If the function succeeds, it registers the callback function and returns 
      <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
      the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

An application that performs I/O directly to a high-performance device typically caches a virtual-to-physical 
    memory mapping for the buffer it uses for the I/O. The device's driver typically secures this memory address range 
    by calling the <a href="/windows-hardware/drivers/ddi/content/ntddk/nf-ntddk-mmsecurevirtualmemory">MmSecureVirtualMemory</a> routine, 
    which prevents the memory range from being freed or its protections  changed until the driver unsecures the 
    memory.

An application can use 
    <b>AddSecureMemoryCacheCallback</b> to register 
    a callback function that will be called when the memory is freed or its protections are changed, so the 
    application can invalidate its cached memory mapping. For more information, see 
    <a href="/windows/desktop/api/winnt/nc-winnt-psecure_memory_cache_callback">SecureMemoryCacheCallback</a>.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0600 
    or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-removesecurememorycachecallback">RemoveSecureMemoryCacheCallback</a>



<a href="/windows/desktop/api/winnt/nc-winnt-psecure_memory_cache_callback">SecureMemoryCacheCallback</a>