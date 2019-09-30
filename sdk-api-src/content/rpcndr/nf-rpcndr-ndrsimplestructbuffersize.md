---
UID: NF:rpcndr.NdrSimpleStructBufferSize
title: NdrSimpleStructBufferSize function (rpcndr.h)
author: windows-sdk-content
description: The NdrSimpleStructBufferSize function calculates the required buffer size, in bytes, to marshal the simple structure.
old-location: winprog\ndrsimplestructbuffersize.htm
tech.root: DevNotes
ms.assetid: e88eaed3-0676-4c43-8ac1-7a5e19fc5748
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NdrSimpleStructBufferSize, NdrSimpleStructBufferSize function [Windows API], rpcndr/NdrSimpleStructBufferSize, winprog.ndrsimplestructbuffersize
ms.topic: function
f1_keywords:
- rpcndr/NdrSimpleStructBufferSize
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
- NdrSimpleStructBufferSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrSimpleStructBufferSize function


## -description


The <b>NdrSimpleStructBufferSize</b> function calculates the required buffer size, in bytes, to marshal the simple structure.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. The <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified. 


### -param pMemory [in]

Pointer to the simple structure to be calculated.


### -param pFormat [in]

Pointer to the format string description.


## -returns



This function has no return values. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a>
 

 

