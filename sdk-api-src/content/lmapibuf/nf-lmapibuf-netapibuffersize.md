---
UID: NF:lmapibuf.NetApiBufferSize
title: NetApiBufferSize function
author: windows-sdk-content
description: The NetApiBufferSize function returns the size, in bytes, of a buffer allocated by a call to the NetApiBufferAllocate function.
old-location: netmgmt\netapibuffersize.htm
old-project: NetMgmt
ms.assetid: 0c28feeb-00a3-4ad5-b85f-96326515fae2
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: NetApiBufferSize, NetApiBufferSize function [Network Management], _win32_netapibuffersize, lmapibuf/NetApiBufferSize, netmgmt.netapibuffersize
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: USER_OTHER_INFO, *PUSER_OTHER_INFO, *LPUSER_OTHER_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetApiBufferSize
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetApiBufferSize function


## -description


The
				<b>NetApiBufferSize</b> function returns the size, in bytes, of a buffer allocated by a call to the 
<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function.


## -parameters




### -param Buffer [in]

Pointer to a buffer returned by the 
<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function.


### -param ByteCount [out]

Receives the size of the buffer, in bytes.


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
 

 

