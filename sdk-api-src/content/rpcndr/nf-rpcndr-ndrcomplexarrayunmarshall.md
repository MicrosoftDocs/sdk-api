---
UID: NF:rpcndr.NdrComplexArrayUnmarshall
title: NdrComplexArrayUnmarshall function
author: windows-sdk-content
description: The NdrComplexArrayUnmarshall function unmarshals the complex array from the network buffer to memory.
old-location: winprog\ndrcomplexarrayunmarshall.htm
tech.root: devnotes
ms.assetid: 2b702bec-e5f4-4bf3-a2d4-d4b901929e53
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: NdrComplexArrayUnmarshall, NdrComplexArrayUnmarshall function [Windows API], rpcndr/NdrComplexArrayUnmarshall, winprog.ndrcomplexarrayunmarshall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - NdrComplexArrayUnmarshall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrComplexArrayUnmarshall function


## -description


The <b>NdrComplexArrayUnmarshall</b> function unmarshals the complex array from the network buffer to memory.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.  


### -param ppMemory [out]

Address to a pointer to the unmarshalled complex array. If set to null, or if the <i>fMustAlloc</i> parameter is set to <b>TRUE</b>, the stub will allocate the memory.


### -param pFormat [in]

Pointer to the format string description.


### -param fMustAlloc [in]

Flag that specifies whether the stub must allocate the memory into which the complex array is to be marshaled.  Specify <b>TRUE</b> if RPC must allocate <i>ppMemory</i>. 


## -returns



Returns null upon success. Raises one of the following exceptions  upon failure.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA or RPC_X_INVALID_BOUND</td>
<td>The network  is incorrect.</td>
</tr>
<tr>
<td>RPC_S_OUT_OF_MEMORY</td>
<td>Out of memory.</td>
</tr>
<tr>
<td>STATUS_ACCESS_VIOLATION</td>
<td>An access violation occurred.</td>
</tr>
<tr>
<td>RPC_S_INTERNAL_ERROR</td>
<td>An error occurred in RPC.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a>
 

 

