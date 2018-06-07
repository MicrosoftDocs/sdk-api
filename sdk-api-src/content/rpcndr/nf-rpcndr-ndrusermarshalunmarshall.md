---
UID: NF:rpcndr.NdrUserMarshalUnmarshall
title: NdrUserMarshalUnmarshall function
author: windows-sdk-content
description: The NdrUserMarshalUnmarshall function calls a user-defined unmarshal routine to unmarshal data with the attribute.
old-location: winprog\ndrusermarshalunmarshall.htm
old-project: DevNotes
ms.assetid: 8012973b-a41f-4729-a04a-8a1afb29cebe
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: NdrUserMarshalUnmarshall, NdrUserMarshalUnmarshall function [Windows API], rpcndr/NdrUserMarshalUnmarshall, winprog.ndrusermarshalunmarshall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
 - NdrUserMarshalUnmarshall
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrUserMarshalUnmarshall function


## -description


The <b>NdrUserMarshalUnmarshall</b> function calls a user-defined unmarshal routine to unmarshal data with the  attribute.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The  <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified.  


### -param ppMemory [in]

Pointer to user data object to be unmarshalled.


### -param pFormat [in]

Format string description of the pointer.


### -param fMustAlloc [in]

Flag that specifies whether the stub must allocate the memory into which the user data object is to be unmarshalled.  Specify <b>TRUE</b> if RPC must allocate <i>ppMemory</i>. 


## -returns



Returns <b>NULL</b> upon success. Returns one of the following exception codes upon error.

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



<a href="https://www.bing.com/search?q=wire_marshal">wire_marshal</a>
 

 

