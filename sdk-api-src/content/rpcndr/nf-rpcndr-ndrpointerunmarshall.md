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

# NdrPointerUnmarshall function


## -description


The <b>NdrPointerUnmarshall</b> function unmarshalls a top level pointer to anything.  Pointers embedded in
    structures, arrays, or unions call <b>NdrPointerUnmarshall</b> directly.



## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param ppMemory

TBD


### -param pFormat [in]

Pointer to the format string description.


### -param fMustAlloc

TBD




#### - fSkipRefCheck [in]

Unused.


#### - pMemory [in]

Pointer to memory where pointer will be unmarshalled. Please see MCCP Buffer Protection for information on buffer overrun protections in RPC: <a href="http://msdn.microsoft.com/en-us/library/ff621497(VS.85).aspx ">http://msdn.microsoft.com/en-us/library/ff621497(VS.85).aspx</a>


## -returns



Returns <b>NULL</b> upon success. If an error occurs, the function throws one of the following exception codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td>RPC_BAD_STUB_DATA or RPC_X_INVALID_BOUND  </td>
<td>The network  buffer is incorrect.</td>
</tr>
<tr>
<td>RPC_S_OUT_OF_MEMORY</td>
<td>The system is out of memory.</td>
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
 




## -remarks



This function is used for FC_RP, FC_UP, FC_FP, FC_OP format strings.




