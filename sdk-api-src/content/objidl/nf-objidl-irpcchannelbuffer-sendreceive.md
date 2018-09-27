---
UID: NF:objidl.IRpcChannelBuffer.SendReceive
title: IRpcChannelBuffer::SendReceive
author: windows-sdk-content
description: Sends a method invocation across an RPC channel to the server stub.
old-location: com\irpcchannelbuffer_sendreceive.htm
tech.root: com
ms.assetid: 8a42fd06-252f-4c1b-bbdb-abc2e3887c46
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IRpcChannelBuffer interface [COM],SendReceive method, IRpcChannelBuffer.SendReceive, IRpcChannelBuffer::SendReceive, SendReceive, SendReceive method [COM], SendReceive method [COM],IRpcChannelBuffer interface, _com_irpcchannelbuffer_sendreceive, com.irpcchannelbuffer_sendreceive, objidlbase/IRpcChannelBuffer::SendReceive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcChannelBuffer.SendReceive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRpcChannelBuffer::SendReceive


## -description


Sends a method invocation across an RPC channel to the server stub.


## -parameters




### -param pMessage [in, out]

A pointer to an <a href="https://msdn.microsoft.com/b4761462-1910-431c-b5cd-c14fdda0b6b6">RPCOLEMESSAGE</a> structure that has been populated with marshaled data.


### -param pStatus [out]

If not <b>NULL</b>, set to 0 on successful execution.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



Before invoking this method, the <a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">GetBuffer</a> method must have been invoked to allocate a channel buffer. Upon return, the <b>dataRepresentation</b> buffer of the <a href="https://msdn.microsoft.com/b4761462-1910-431c-b5cd-c14fdda0b6b6">RPCOLEMESSAGE</a> structure will have been modified to include the data returned by the method invoked on the server. If the invocation was successful, the RPC channel buffer has been freed; otherwise the caller must free it explicitly by calling <a href="https://msdn.microsoft.com/bcdd4783-4a75-42d0-86a9-ab2605abbbe1">FreeBuffer</a>.




## -see-also




<a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a>
 

 

