---
UID: NF:rpcndr.NdrComplexArrayBufferSize
title: NdrComplexArrayBufferSize function
author: windows-sdk-content
description: The NdrComplexArrayBufferSize function calculates the required buffer size, in bytes, to marshal the complex array.
old-location: winprog\ndrcomplexarraybuffersize.htm
tech.root: devnotes
ms.assetid: 8efd63c5-7444-4b30-b642-18dfecb7d026
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: NdrComplexArrayBufferSize, NdrComplexArrayBufferSize function [Windows API], rpcndr/NdrComplexArrayBufferSize, winprog.ndrcomplexarraybuffersize
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
 - NdrComplexArrayBufferSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NdrComplexArrayBufferSize function


## -description


The <b>NdrComplexArrayBufferSize</b> function calculates the required buffer size, in bytes, to marshal the complex array.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. The <b>MIDL_STUB_MESSAGE</b> structure is for internal use only, and must not be modified. 


### -param pMemory [in]

Pointer to the  complex array to be calculated.


### -param pFormat [in]

Pointer to the format string description.


## -returns



This function has no return values. 




## -see-also




<a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a>
 

 

