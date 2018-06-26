---
UID: NF:objidl.IRpcChannelBuffer.FreeBuffer
title: IRpcChannelBuffer::FreeBuffer
author: windows-sdk-content
description: Frees a previously allocated RPC channel buffer.
old-location: com\irpcchannelbuffer_freebuffer.htm
old-project: com
ms.assetid: bcdd4783-4a75-42d0-86a9-ab2605abbbe1
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: FreeBuffer, FreeBuffer method [COM], FreeBuffer method [COM],IRpcChannelBuffer interface, IRpcChannelBuffer interface [COM],FreeBuffer method, IRpcChannelBuffer.FreeBuffer, IRpcChannelBuffer::FreeBuffer, _com_irpcchannelbuffer_freebuffer, com.irpcchannelbuffer_freebuffer, objidlbase/IRpcChannelBuffer::FreeBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcChannelBuffer.FreeBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IRpcChannelBuffer::FreeBuffer


## -description


Frees a previously allocated RPC channel buffer.


## -parameters




### -param pMessage [in, out]

A pointer to an <a href="https://msdn.microsoft.com/b4761462-1910-431c-b5cd-c14fdda0b6b6">RPCOLEMESSAGE</a> data structure.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>
 

 

