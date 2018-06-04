---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# NetApiBufferFree function


## -description


The
				<b>NetApiBufferFree</b> function frees the memory that the 
<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function allocates. Applications should also call <b>NetApiBufferFree</b> to free the memory that other network management functions use internally to return information.


## -parameters




### -param Buffer [in]

A pointer to a buffer returned previously by another network management function or memory allocated by calling the <a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The
				<b>NetApiBufferFree</b> function is used to free memory used by network management functions. This function is used in two cases:


<ul>
<li> To free memory explicitly allocated by calls in an application to the <a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function when the memory is no longer needed.</li>
<li>To free memory allocated internally by calls in an application to remotable network management functions that return information to the caller. The RPC run-time library internally allocates the buffer containing the return information. </li>
</ul>


Many network management functions retrieve information and return this information as a buffer that may contain a complex structure, an array of structures, or an array of nested structures. These functions use the RPC run-time library to internally allocate the buffer containing the return information, whether the call is to a local computer or a remote server. For example, the <a href="https://msdn.microsoft.com/10012a87-805e-4817-9f09-9e5632b1fa09">NetServerEnum</a> function retrieves a lists of servers and returns this information as an array of  structures pointed to by the <i>bufptr</i> parameter. When the function is successful, memory is allocated internally by the  <b>NetServerEnum</b> function to store the array of structures returned in the <i>bufptr</i> parameter to the application. When this array of structures is no longer needed,  the <b>NetApiBufferFree</b> function should be called by the application with the <i>Buffer</i> parameter set to the <i>bufptr</i> parameter returned by  <b>NetServerEnum</b> to free this internal memory used. In these cases, the <b>NetApiBufferFree</b> function frees all of the internal memory allocated for the buffer including memory for nested structures, pointers to strings, and other data.

No special group membership is required to successfully execute the <b>NetApiBufferFree</b> function or any of the other <a href="https://msdn.microsoft.com/bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18">ApiBuffer functions</a>.

For a code sample that demonstrates how to use of the <b>NetApiBufferFree</b> function to free memory explicitly allocated by an application, see 
the <a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a> function.

For a code sample that demonstrates how to use of the <b>NetApiBufferFree</b> function to free memory internally allocated by a network management function to return information, see 
the <a href="https://msdn.microsoft.com/10012a87-805e-4817-9f09-9e5632b1fa09">NetServerEnum</a> function.




## -see-also




<a href="https://msdn.microsoft.com/bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18">Api Buffer
		  Functions</a>



<a href="https://msdn.microsoft.com/9ff1e3eb-9417-469f-a8c0-cdcda3cd9583">NetApiBufferAllocate</a>



<a href="https://msdn.microsoft.com/61153de0-33d3-4c83-a8aa-a7179252328c">NetApiBufferReallocate</a>



<a href="https://msdn.microsoft.com/0c28feeb-00a3-4ad5-b85f-96326515fae2">NetApiBufferSize</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>



<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>
 

 

