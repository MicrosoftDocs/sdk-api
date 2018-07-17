---
UID: NF:objidlbase.IRpcStubBuffer.Invoke
title: IRpcStubBuffer::Invoke
author: windows-sdk-content
description: Invokes the interface that a stub represents.
old-location: com\irpcstubbuffer_invoke.htm
old-project: com
ms.assetid: 78d20830-78d7-4395-aaec-8a86b7c41cc7
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IRpcStubBuffer interface [COM],Invoke method, IRpcStubBuffer.Invoke, IRpcStubBuffer::Invoke, Invoke, Invoke method [COM], Invoke method [COM],IRpcStubBuffer interface, _com_irpcstubbuffer_invoke, com.irpcstubbuffer_invoke, objidlbase/IRpcStubBuffer::Invoke
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
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
 - IRpcStubBuffer.Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IRpcStubBuffer::Invoke


## -description


Invokes the interface that a stub represents.


## -parameters




### -param _prpcmsg [in, out]

A pointer to an <a href="https://msdn.microsoft.com/b4761462-1910-431c-b5cd-c14fdda0b6b6">RPCOLEMESSAGE</a> data structure containing the marshaled invocation arguments.


### -param _pRpcChannelBuffer [in]

A pointer to an <a href="https://msdn.microsoft.com/1d7d7e1c-a491-4625-97ae-0d4dc5d2fc20">IRpcChannelBuffer</a> interface that controls an RPC marshaling channel.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/0aa724f0-6110-4ebf-a0c1-d309074a61d9">IRpcStubBuffer</a>
 

 

