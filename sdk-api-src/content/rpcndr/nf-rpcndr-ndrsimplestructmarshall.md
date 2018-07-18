---
UID: NF:rpcndr.NdrSimpleStructMarshall
title: NdrSimpleStructMarshall function
author: windows-sdk-content
description: The NdrSimpleStructMarshall function marshals the simple structure into a network buffer.
old-location: winprog\ndrsimplestructmarshall.htm
old-project: devnotes
ms.assetid: 9e921653-0669-4fe9-8a54-509ed39ad204
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: NdrSimpleStructMarshall, NdrSimpleStructMarshall function [Windows API], rpcndr/NdrSimpleStructMarshall, winprog.ndrsimplestructmarshall
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - NdrSimpleStructMarshall
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# NdrSimpleStructMarshall function


## -description


The <b>NdrSimpleStructMarshall</b> function marshals the simple structure into a network buffer.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.


### -param pMemory [in]

Pointer to the simple structure to be marshaled.


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
 

 

