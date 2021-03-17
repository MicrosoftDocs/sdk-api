---
UID: NF:lmapibuf.NetApiBufferFree
title: NetApiBufferFree function (lmapibuf.h)
description: The NetApiBufferFree function frees the memory that the NetApiBufferAllocate function allocates. Applications should also call NetApiBufferFree to free the memory that other network management functions use internally to return information.
helpviewer_keywords: ["NetApiBufferFree","NetApiBufferFree function [Network Management]","_win32_netapibufferfree","lmapibuf/NetApiBufferFree","netmgmt.netapibufferfree"]
old-location: netmgmt\netapibufferfree.htm
tech.root: NetMgmt
ms.assetid: 0e99483c-8cd7-402a-8bf6-1e0118764dd3
ms.date: 12/05/2018
ms.keywords: NetApiBufferFree, NetApiBufferFree function [Network Management], _win32_netapibufferfree, lmapibuf/NetApiBufferFree, netmgmt.netapibufferfree
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetApiBufferFree
 - lmapibuf/NetApiBufferFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - Netutils.dll
api_name:
 - NetApiBufferFree
---

# NetApiBufferFree function


## -description

The
				<b>NetApiBufferFree</b> function frees the memory that the 
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function allocates. Applications should also call <b>NetApiBufferFree</b> to free the memory that other network management functions use internally to return information.

## -parameters

### -param Buffer [in]

A pointer to a buffer returned previously by another network management function or memory allocated by calling the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function.

## -returns

If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
<a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

The
				<b>NetApiBufferFree</b> function is used to free memory used by network management functions. This function is used in two cases:


<ul>
<li> To free memory explicitly allocated by calls in an application to the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function when the memory is no longer needed.</li>
<li>To free memory allocated internally by calls in an application to remotable network management functions that return information to the caller. The RPC run-time library internally allocates the buffer containing the return information. </li>
</ul>


Many network management functions retrieve information and return this information as a buffer that may contain a complex structure, an array of structures, or an array of nested structures. These functions use the RPC run-time library to internally allocate the buffer containing the return information, whether the call is to a local computer or a remote server. For example, the <a href="/windows/desktop/api/lmserver/nf-lmserver-netserverenum">NetServerEnum</a> function retrieves a lists of servers and returns this information as an array of  structures pointed to by the <i>bufptr</i> parameter. When the function is successful, memory is allocated internally by the  <b>NetServerEnum</b> function to store the array of structures returned in the <i>bufptr</i> parameter to the application. When this array of structures is no longer needed,  the <b>NetApiBufferFree</b> function should be called by the application with the <i>Buffer</i> parameter set to the <i>bufptr</i> parameter returned by  <b>NetServerEnum</b> to free this internal memory used. In these cases, the <b>NetApiBufferFree</b> function frees all of the internal memory allocated for the buffer including memory for nested structures, pointers to strings, and other data.

No special group membership is required to successfully execute the <b>NetApiBufferFree</b> function or any of the other <a href="/windows/desktop/NetMgmt/apibuffer-functions">ApiBuffer functions</a>.

For a code sample that demonstrates how to use of the <b>NetApiBufferFree</b> function to free memory explicitly allocated by an application, see 
the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a> function.

For a code sample that demonstrates how to use of the <b>NetApiBufferFree</b> function to free memory internally allocated by a network management function to return information, see 
the <a href="/windows/desktop/api/lmserver/nf-lmserver-netserverenum">NetServerEnum</a> function.

## -see-also

<a href="/windows/desktop/NetMgmt/apibuffer-functions">Api Buffer
		  Functions</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferallocate">NetApiBufferAllocate</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferreallocate">NetApiBufferReallocate</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibuffersize">NetApiBufferSize</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>



<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>