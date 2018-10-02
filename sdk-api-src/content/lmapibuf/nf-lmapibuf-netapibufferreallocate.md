---
UID: NF:lmapibuf.NetApiBufferReallocate
title: NetApiBufferReallocate function
author: windows-sdk-content
description: The NetApiBufferReallocate function changes the size of a buffer allocated by a previous call to the NetApiBufferAllocate function.
old-location: netmgmt\netapibufferreallocate.htm
tech.root: NetMgmt
ms.assetid: 61153de0-33d3-4c83-a8aa-a7179252328c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NetApiBufferReallocate, NetApiBufferReallocate function [Network Management], _win32_netapibufferreallocate, lmapibuf/NetApiBufferReallocate, netmgmt.netapibufferreallocate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmapibuf.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetApiBufferReallocate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetApiBufferReallocate function


## -description


The 
				<b>NetApiBufferReallocate</b> function changes the size of a buffer allocated by a previous call to the 
<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function.


## -parameters




### -param OldBuffer [in]

Pointer to the buffer returned by a call to the 
<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function.


### -param NewByteCount [in]

Specifies the new size of the buffer, in bytes.


### -param NewBuffer [out]

Receives the pointer to the reallocated buffer.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



No special group membership is required to successfully execute the ApiBuffer functions.

For a code sample that demonstrates how to use the network management 
<a href="https://msdn.microsoft.com/bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18">ApiBuffer functions</a>, see 
<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a>.




## -see-also




<a href="https://msdn.microsoft.com/bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18">Api Buffer
		  Functions</a>



<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

