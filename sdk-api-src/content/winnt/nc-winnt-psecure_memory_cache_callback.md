---
UID: NC:winnt.PSECURE_MEMORY_CACHE_CALLBACK
title: PSECURE_MEMORY_CACHE_CALLBACK
author: windows-sdk-content
description: An application-defined function previously registered with the AddSecureMemoryCacheCallback function that is called when a secured memory range is freed or its protections are changed.
old-location: base\securememorycachecallback.htm
tech.root: Memory
ms.assetid: abde4b6f-7cd8-4a4b-9b00-f035b2c29054
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PSECURE_MEMORY_CACHE_CALLBACK, PSECURE_MEMORY_CACHE_CALLBACK callback function, SecureMemoryCacheCallback, SecureMemoryCacheCallback callback, SecureMemoryCacheCallback callback function, base.securememorycachecallback, winnt/PSECURE_MEMORY_CACHE_CALLBACK, winnt/SecureMemoryCacheCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNT.h
api_name:
 - SecureMemoryCacheCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PSECURE_MEMORY_CACHE_CALLBACK callback function


## -description


An application-defined function previously registered with the 
    <a href="https://msdn.microsoft.com/6c89d6f3-182e-4b10-931c-8d55d603c9dc">AddSecureMemoryCacheCallback</a> function 
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
    <a href="http://go.microsoft.com/fwlink/p/?linkid=99148">MmSecureVirtualMemory</a> and 
    <a href="http://go.microsoft.com/fwlink/p/?linkid=100741">MmUnsecureVirtualMemory</a> 
    functions to actually secure and unsecure the range. Operations on other types of secured or locked memory do not 
    trigger this callback.

Examples of function calls that trigger the callback function include calls to the 
    <a href="https://msdn.microsoft.com/d6f27be8-8929-4a4d-b52c-fa99044ca243">VirtualFree</a>, 
    <a href="https://msdn.microsoft.com/2e5c862c-1251-49da-9c3a-90b09e488d89">VirtualFreeEx</a>, 
    <a href="https://msdn.microsoft.com/a0018bba-226b-4c18-8ea4-15e69524db11">VirtualProtect</a>, 
    <a href="https://msdn.microsoft.com/6afd7ae6-e4c5-483c-a638-c85781674c7b">VirtualProtectEx</a>, and 
    <a href="https://msdn.microsoft.com/2e9c3174-af48-4fa3-9f6a-fb62b23ed994">UnmapViewOfFile</a> functions.

The callback function can also be triggered by a heap operation. In this case, the function must not perform 
    any further operations on the heap that triggered the callback. This includes calling 
    <a href="https://msdn.microsoft.com/cfb683fa-4f46-48b5-9a28-f4625a9cb8cd">heap functions</a> on a private heap or the process's default 
    heap, or calling standard library functions such as <b>malloc</b> and 
    <b>free</b>, which implicitly use the process's default heap.

To unregister the callback function, use the 
    <a href="https://msdn.microsoft.com/8be6ff04-34c7-4942-a38c-507584c8bbeb">RemoveSecureMemoryCacheCallback</a> 
    function.




## -see-also




<a href="https://msdn.microsoft.com/6c89d6f3-182e-4b10-931c-8d55d603c9dc">AddSecureMemoryCacheCallback</a>



<a href="https://msdn.microsoft.com/8be6ff04-34c7-4942-a38c-507584c8bbeb">RemoveSecureMemoryCacheCallback</a>
 

 

