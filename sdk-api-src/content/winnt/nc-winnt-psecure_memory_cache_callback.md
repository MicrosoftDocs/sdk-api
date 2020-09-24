---
UID: NC:winnt.PSECURE_MEMORY_CACHE_CALLBACK
title: PSECURE_MEMORY_CACHE_CALLBACK (winnt.h)
description: An application-defined function previously registered with the AddSecureMemoryCacheCallback function that is called when a secured memory range is freed or its protections are changed.
helpviewer_keywords: ["PSECURE_MEMORY_CACHE_CALLBACK","PSECURE_MEMORY_CACHE_CALLBACK callback function","SecureMemoryCacheCallback","SecureMemoryCacheCallback callback","SecureMemoryCacheCallback callback function","base.securememorycachecallback","winnt/PSECURE_MEMORY_CACHE_CALLBACK","winnt/SecureMemoryCacheCallback"]
old-location: base\securememorycachecallback.htm
tech.root: base
ms.assetid: abde4b6f-7cd8-4a4b-9b00-f035b2c29054
ms.date: 12/05/2018
ms.keywords: PSECURE_MEMORY_CACHE_CALLBACK, PSECURE_MEMORY_CACHE_CALLBACK callback function, SecureMemoryCacheCallback, SecureMemoryCacheCallback callback, SecureMemoryCacheCallback callback function, base.securememorycachecallback, winnt/PSECURE_MEMORY_CACHE_CALLBACK, winnt/SecureMemoryCacheCallback
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PSECURE_MEMORY_CACHE_CALLBACK
 - winnt/PSECURE_MEMORY_CACHE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNT.h
api_name:
 - SecureMemoryCacheCallback
---

# PSECURE_MEMORY_CACHE_CALLBACK callback function


## -description

An application-defined function previously registered with the 
    <a href="/windows/desktop/api/winbase/nf-winbase-addsecurememorycachecallback">AddSecureMemoryCacheCallback</a> function 
    that is called when a secured memory range is freed or its protections are changed.

The <b>PSECURE_MEMORY_CACHE_CALLBACK</b> type defines a pointer to this callback 
    function. <i>SecureMemoryCacheCallback</i> is a 
    placeholder for the application-defined function name.

## -parameters

### -param Addr [in]

The starting address of the memory range.

### -param Range [in]

The size of the memory range, in bytes.

## -returns

The return value indicates the success or failure of this function.

If the caller has secured the specified memory range, this function should unsecure the memory and return 
       <b>TRUE</b>.

If the caller has not secured the specified memory range, this function should return 
       <b>FALSE</b>.

## -remarks

After the callback function is registered, it is called after any attempt to free the specified memory range 
    or change its protections. If the application has secured any part of the specified memory range, the callback 
    function must invalidate all of the application's cached memory mappings for the secured memory range, unsecure 
    the secured parts of the memory range, and return <b>TRUE</b>. Otherwise it must  return 
    <b>FALSE</b>.

The application secures and unsecures a memory range by sending requests to a device driver, which uses the 
    MmSecureVirtualMemory and 
    MmUnsecureVirtualMemory 
    functions to actually secure and unsecure the range. Operations on other types of secured or locked memory do not 
    trigger this callback.

Examples of function calls that trigger the callback function include calls to the 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfree">VirtualFree</a>, 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualfreeex">VirtualFreeEx</a>, 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect">VirtualProtect</a>, 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotectex">VirtualProtectEx</a>, and 
    <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a> functions.

The callback function can also be triggered by a heap operation. In this case, the function must not perform 
    any further operations on the heap that triggered the callback. This includes calling 
    <a href="/windows/desktop/Memory/heap-functions">heap functions</a> on a private heap or the process's default 
    heap, or calling standard library functions such as <b>malloc</b> and 
    <b>free</b>, which implicitly use the process's default heap.

To unregister the callback function, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-removesecurememorycachecallback">RemoveSecureMemoryCacheCallback</a> 
    function.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-addsecurememorycachecallback">AddSecureMemoryCacheCallback</a>



<a href="/windows/desktop/api/winbase/nf-winbase-removesecurememorycachecallback">RemoveSecureMemoryCacheCallback</a>