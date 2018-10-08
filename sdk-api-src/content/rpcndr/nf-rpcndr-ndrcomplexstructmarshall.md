---
UID: NF:rpcndr.NdrComplexStructMarshall
title: NdrComplexStructMarshall function
author: windows-sdk-content
description: The NdrComplexStructMarshall function marshals the complex structure into a network buffer.
old-location: winprog\ndrcomplexstructmarshall.htm
tech.root: devnotes
ms.assetid: 722c274e-1c66-4b46-b243-02eeaaad1f6b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: NdrComplexStructMarshall, NdrComplexStructMarshall function [Windows API], rpcndr/NdrComplexStructMarshall, winprog.ndrcomplexstructmarshall
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
 - NdrComplexStructMarshall
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrComplexStructMarshall function


## -description


The <b>NdrComplexStructMarshall</b> function marshals the complex structure into a network buffer.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.


### -param pMemory [in]

Pointer to the complex structure to be marshaled.


### -param pFormat [in]

Pointer to the format string description.


## -returns



Returns null upon success. Raises one of the following exceptions upon failure.

<table>
<tr>
<th>Error</th>
<th>Description</th>
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
 

 

